# 🔐 SSH Brute Force Detection & Response

![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![Platform](https://img.shields.io/badge/SIEM-Splunk-orange)
![ATT&CK](https://img.shields.io/badge/MITRE-T1110.001-red)
![Verdict](https://img.shields.io/badge/Verdict-True%20Positive-critical)

## Overview

A simulated SSH brute-force attack was conducted against a Linux host in a controlled home lab environment. Authentication logs were forwarded to Splunk for SIEM correlation, threat analysis, and incident documentation — following a structured Detect → Analyze → Contain → Escalate (DACE) response framework.

## Lab Environment

| Role | OS | IP |
|---|---|---|
| 🗡️ Attacker | Kali Linux | **`192.168.56.12`** |
| 🎯 Victim | Ubuntu Linux | **`192.168.56.111`** |
| 🖥️ Monitoring | Ubuntu Linux + Splunk | **`192.168.56.10`** |

**Stack:** Splunk Enterprise · Splunk Universal Forwarder · Hydra · Kali Linux


## Attack Simulation

Technique: Dictionary-based brute-force attack was launched from the Kali machine against the SSH service (port 22) on `192.168.56.111` using Hydra and a password list.

<img width="736" height="827" alt="hydra_ssh_brute_force" src="https://github.com/user-attachments/assets/9699fea1-fc94-45bd-b197-2714b2b5cc3c" />

**Result:** Multiple rapid failed authentications followed by a successful login using a valid credential obtained from the list.


## Detection

Authentication logs were forwarded via Splunk Universal Forwarder and queried for anomalous login behavior.

**Failed login query:**
```spl
index=* sourcetype=linux_secure "Failed password"
| stats count by src_ip, user, _time
```
<img width="1137" height="751" alt="splunk_failed_logs" src="https://github.com/user-attachments/assets/c9bed3b2-e487-40f8-937d-ac2e79c8a5db" />

**Failed logins count:**

<img width="1837" height="318" alt="splunk_failed_counts" src="https://github.com/user-attachments/assets/cb3c3f28-2994-4962-b355-348255e8be18" />


**Successful login query:**
```spl
index=* sourcetype=linux_secure "Accepted password"
| stats count by src_ip, user, _time
```
<img width="1016" height="82" alt="splunk_successful_login" src="https://github.com/user-attachments/assets/e644f8ae-d375-4d21-bac1-54cf44277724" />

**Key findings:**
- `28` failed SSH authentication attempts within under two minute window from a single source IP (`192.168.56.12`)
- Immediately followed by one successful authentication
- All attempts targeted the same account from the same IP
  

## Analysis

### Indicators of Compromise (IOCs)

| Type | Value | Notes |
|---|---|---|
| Source IP | `192.168.56.12` | Kali attacker machine |
| Target IP | `192.168.56.111` | Victim host |
| Target Service | SSH / Port 22 | |
| Auth Pattern | 20+ failures → 1 success | Brute force signature |
| Compromised Account | [target] | Credential confirmed valid |

### Verdict

> ✅ **TRUE POSITIVE — Account Compromise Confirmed**
>
> High-volume failed authentications in a compressed timeframe is a definitive brute force indicator. A successful login immediately following failed attempts confirms credential compromise. Single-source IP rules out distributed attack and confirms targeted brute force consistent with Hydra-style automated credential stuffing.




## MITRE ATT&CK Mapping

| Tactic | Technique | ID |
|---|---|---|
| Credential Access | Brute Force: Password Guessing | [T1110.001](https://attack.mitre.org/techniques/T1110/001/) |
| Initial Access | Valid Accounts | [T1078](https://attack.mitre.org/techniques/T1078/) |
| Lateral Movement | Remote Services: SSH | [T1021.004](https://attack.mitre.org/techniques/T1021/004/) |



## Response

### Containment Actions
 
| Priority | Action |
|---|---|
| Immediate | Reset compromised credentials |
| Immediate | Block attacker IP at firewall level |
| Immediate | Lock affected account pending full investigation |
| Follow-up | Review post-login activity for lateral movement or privilege escalation |
| Follow-up | Audit all systems accessible by the compromised account |


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

## Log Ingestion & Discrepancy Analysis

    Attacker Metric (Hydra): The tool executed 45 total authentication attempts before identifying the correct credential.

    SIEM Metric (Splunk): The dashboard indexed exactly 30 failed login events during the 2-minute and 32-second attack window.

Root-Cause Findings: > A post-incident investigation was conducted by checking the target server's local system logs (/var/log/auth.log). The local logs confirmed only 30 events were ever generated.

This proves that the 15 missing attempts were dropped at the host network/OS layer because Hydra’s aggressive multi-threading overwhelmed the SSH daemon, causing it to drop TCP connections before the operating system could process and log the login attempt.

---

## References

- [MITRE ATT&CK T1110.001 — Brute Force: Password Guessing](https://attack.mitre.org/techniques/T1110/001/)
- [MITRE ATT&CK T1078 — Valid Accounts](https://attack.mitre.org/techniques/T1078/)
- [MITRE ATT&CK T1021.004 — Remote Services: SSH](https://attack.mitre.org/techniques/T1021/004/)
- [Splunk Documentation](https://docs.splunk.com)
