# 🔐 SSH Brute Force Detection & Response

![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![Platform](https://img.shields.io/badge/SIEM-Splunk-orange)
![ATT&CK](https://img.shields.io/badge/MITRE-T1110.001-red)
![Verdict](https://img.shields.io/badge/Verdict-True%20Positive-critical)

## Overview

A simulated SSH brute-force attack was conducted against a Linux host in a controlled home lab environment. Authentication logs were forwarded to Splunk for SIEM correlation, threat analysis, and incident documentation — following a structured Detect → Analyze → Contain → Escalate (DACE) response framework.

---

## Lab Environment

| Role | OS | IP |
|---|---|---|
| 🗡️ Attacker | Kali Linux | 192.168.56.12 |
| 🎯 Victim | Ubuntu Linux | 192.168.56.111 |
| 🖥️ Monitoring | Ubuntu Linux + Splunk | 192.168.56.10 |

**Stack:** Splunk Enterprise · Splunk Universal Forwarder · Hydra · Kali Linux

---

## Attack Simulation

A credential stuffing attack was launched from the Kali machine against the SSH service (port 22) on `192.168.56.111` using Hydra and a password list.

**Result:** Multiple rapid failed authentications followed by a successful login using a valid credential obtained from the list.

---

## Detection

Authentication logs were forwarded via Splunk Universal Forwarder and queried for anomalous login behavior.

**Failed login query:**
```spl
index=* sourcetype=linux_secure "Failed password"
| stats count by src_ip, user, _time
```

**Successful login query:**
```spl
index=* sourcetype=linux_secure "Accepted password"
| stats count by src_ip, user, _time
```

**Key findings:**
- `20+` failed SSH authentication attempts within under one minute from a single source IP
- Immediately followed by one successful authentication
- All attempts targeted the same account from the same IP

> 📸 See `/screenshots` for Splunk query output

---

## Analysis

### Indicators of Compromise (IOCs)

| Type | Value | Notes |
|---|---|---|
| Source IP | `192.168.56.12` | Kali attacker machine |
| Target IP | `192.168.56.111` | Victim host |
| Target Service | SSH / Port 22 | |
| Auth Pattern | 20+ failures → 1 success | Brute force signature |
| Compromised Account | [username] | Credential confirmed valid |

### Verdict

> ✅ **TRUE POSITIVE — Account Compromise Confirmed**

**Reasoning:**
- High-volume failed authentications in a compressed timeframe is a definitive brute force indicator
- Successful login immediately following failed attempts confirms credential compromise
- Single-source IP rules out distributed attack — confirms targeted brute force
- Pattern consistent with Hydra-style automated credential stuffing

---

## MITRE ATT&CK Mapping

| Tactic | Technique | ID |
|---|---|---|
| Credential Access | Brute Force: Password Guessing | [T1110.001](https://attack.mitre.org/techniques/T1110/001/) |
| Initial Access | Valid Accounts | [T1078](https://attack.mitre.org/techniques/T1078/) |
| Lateral Movement | Remote Services: SSH | [T1021.004](https://attack.mitre.org/techniques/T1021/004/) |

---

## Response

### Containment Actions
- 🔑 Reset compromised credentials immediately
- 🚫 Block attacker IP at firewall level
- 🔒 Temporarily lock affected account pending investigation
- 🔍 Review post-login activity for lateral movement, privilege escalation, or outbound connections

### Evidence Preserved
- Splunk query results (CSV export)
- Raw `/var/log/auth.log` entries from victim machine
- Full event timeline with timestamps

---

## L2 Escalation Handoff

| Field | Detail |
|---|---|
| **What was seen** | Successful SSH brute force against `192.168.56.111` — 20+ failed attempts followed by confirmed account compromise |
| **What was checked** | SIEM correlation via Splunk, auth log review, source IP analysis, post-login activity |
| **What's next** | Determine lateral movement scope, audit all systems accessible by compromised account, consider org-wide credential review |
| **Severity** | 🔴 High |
| **Status** | Confirmed True Positive — Escalated to L2 |

---

## Key Takeaways

- High-volume failed authentications in a short window is a reliable brute force indicator even without pre-configured alerts
- A successful login immediately following failures must be treated as account compromise until ruled out
- When one anomaly is discovered, always check surrounding context — one compromised account may indicate broader exposure
- MITRE ATT&CK mapping accelerates L2 handoff by providing immediate attack chain context

---

## References

- [MITRE ATT&CK T1110.001 — Brute Force: Password Guessing](https://attack.mitre.org/techniques/T1110/001/)
- [MITRE ATT&CK T1078 — Valid Accounts](https://attack.mitre.org/techniques/T1078/)
- [MITRE ATT&CK T1021.004 — Remote Services: SSH](https://attack.mitre.org/techniques/T1021/004/)
- [Splunk Documentation](https://docs.splunk.com)
