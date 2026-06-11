# Cybersecurity Portfolio

This repository contains a curated collection of portfolio documents, technical labs, and risk assessments showcasing foundational work in cybersecurity. The projects documented below demonstrate hands-on application across security monitoring, identity and access management (IAM), systems administration, and governance, risk, and compliance (GRC).

---

## Technical Skills & Core Tools

| Domain | Core Competencies | Technologies & Frameworks |
| :--- | :--- | :--- |
| **Security Operations** | Log Management, Network Defense, Incident Triage | `Splunk (SIEM)` `tcpdump` `Wireshark` |
| **Infrastructure & Protocols** | Systems Administration, Network Security | `Linux CLI` `SSH` `Firewalls` `TCP/IP` `DNS` `HTTP` |
| **Automation & Scripting** | Security Scripting, Data Parsing | `Python` |
| **Frameworks & GRC** | Threat Modeling, Risk Auditing, Access Review | `MITRE ATT&CK` `NIST CSF` `PASTA` `AAA Principles` |

---

## Portfolio Architecture

To review specific project documentation, objectives, and technical outcomes, navigate through the specialized security domains below:

* **`01.`** **[Security Operations & Incident Response](#1-security-operations--incident-response)** ↳ *SIEM analysis, packet captures, brute-force tracking, and network containment.*
* **`02.`** **[Identity & Access Management (IAM)](#2-identity--access-management-iam)** ↳ *Authentication auditing, access control models, and network hardening.*
* **`03.`** **[Security Automation & Systems Administration](#3-security-automation--systems-administration)** ↳ *Python access-control scripting and Linux file-system permission management.*
* **`04.`** **[Governance, Risk, & Compliance (GRC)](#4-governance-risk--compliance-grc)** ↳ *NIST CSF alignment, PASTA threat modeling, and prioritized enterprise risk registers.*

---

## 1. Security Operations & Incident Response

<details>
<summary><b>Host-Based Intrusion Detection & SIEM Analysis (SSH Brute Force)</b></summary>
<br>

*📁 Core Lab:* **[Linux Authentication Brute Force Analysis](./path-to-your-file)** | *Tech Stack:* `Splunk (SIEM)` `Linux CLI` `/var/log/auth.log` `MITRE ATT&CK`
> **Objective:** Analyzed a simulated SSH brute-force attack against a Linux target host (`192.168.56.111`) using a password list.
> 
> **Outcome:** Identified multiple failed authentication attempts followed by a successful login using valid credentials. Validated the malicious activity through host logs and Splunk SIEM correlation, and documented the findings using MITRE ATT&CK mapping.
</details>

<details>
<summary><b>Network-Layer Incident Investigation (SYN Flood)</b></summary>
<br>

*📁 Core Lab:* **[Analyzing Network Attacks for Travel Agency](./security-incident-reports/SIR%20-%20Analyzing%20Network%20Attacks.pdf)** | *Tech Stack:* `Firewall Configuration` `Traffic Analysis`
> **Objective:** Responded to an alert regarding server issues for a travel agency website.
> 
> **Outcome:** Investigated traffic logs to identify a high volume of TCP SYN requests from an unfamiliar IP address. Documented the incident, temporarily took the server offline to recover, and blocked the offending IP address through firewall configuration.
</details>

<details>
<summary><b>Network Traffic Analysis & Protocol Exploitation </b></summary>
<br>

*📁 Core Lab:* **[Network Traffic Analysis via tcpdump](./security-incident-reports/SIR%20-%20Network%20Traffic%20Analysis.pdf)** | *Tech Stack:* `tcpdump` `DNS Logs` `HTTP Logs` `Network Protocols`
> **Objective:** Investigated a recurring security breach affecting `YummyRecipesForMe.com` by analyzing DNS and HTTP traffic logs following a suspected brute-force attack.
> 
> **Outcome:** Utilized `tcpdump` logs to examine packet details and track the lifecycle of the attack. Identified the specific network protocols and exploitation techniques used by the threat actor, and formulated an action plan with targeted security controls to mitigate future protocol-level vulnerabilities.
</details>

<details>
<summary><b>Phishing Triage & Playbook Execution</b></summary>
<br>

*📁 Core Lab:* **[Playbook Response to Phishing Incident](./playbook-response-to-phishing-incident)** | *Tech Stack:* `Incident Response Playbook` `File Hash Verification` `SHA-256`
> **Objective:** Responded to a phishing incident at a financial services company where a suspicious file was downloaded from an email.
> 
> **Outcome:** Followed the organization's security policies and incident response playbook to analyze the malicious file, document details (including the file hash) in the alert ticket, and secure the affected system.
</details>

<details>
<summary><b>DDoS Mitigation & Incident Reporting</b></summary>
<br>

*📁 Core Lab:* **[NIST CSF Incident Response for Multimedia Company](./security-incident-response/Incident%20Report%20Analysis%20-%20Utilizing%20NIST%20CSF%20for%20Security%20Incident%20Response.pdf)** | *Tech Stack:* `NIST CSF` `Network Security Planning` `ICMP Flood`
> **Objective:** Analyzed a DDoS attack (ICMP packet flood) that disrupted a multimedia company's internal network services for two hours.
> 
> **Outcome:** Applied the NIST Cybersecurity Framework to analyze the incident, document the response actions, and develop a network security plan to mitigate similar threats.
</details>

---

## 2. Identity & Access Management (IAM)

<details>
<summary><b>Post-Incident Access Control Assessment</b></summary>
<br>

*📁 Core Lab:* **[Improving Authentication, Authorization, and Accounting for Growing Business](./access-control-assessment/Access%20Controls%20Assessment.pdf)** | *Tech Stack:* `Access Log Auditing` `AAA Principles` `Vulnerability Identification`
> **Objective:** Assessed access controls following an incident where an unauthorized deposit was made to an unknown bank account.
> 
> **Outcome:** Reviewed access logs to identify potential threat actors and pinpoint vulnerabilities in the access control system, resulting in recommendations to improve access controls and prevent future incidents.
</details>

<details>
<summary><b>Defense-in-Depth & Network Hardening</b></summary>
<br>

*📁 Core Lab:* **[Network Hardening for Social Media Organization](./security-risk-assessment-report/Security%20Risk%20Assessment%20Report%20-%20Analysis%20of%20Network%20Hardening.pdf)** | *Tech Stack:* `Network Hardening Tools` `Vulnerability Assessment`
> **Objective:** Addressed a major data breach experienced by a social media organization due to undetected network vulnerabilities.
> 
> **Outcome:** Identified common network hardening tools, selected a specific network vulnerability, and proposed targeted hardening methods to prevent future breaches.
</details>

---

## 3. Security Automation & Systems Administration

<details>
<summary><b>Automated Access Control via Python</b></summary>
<br>

*📁 Core Lab:* **[Access Control Update for Health Care Company](./file-update-through-a-python-algorithm/Updating%20a%20File%20through%20a%20Python%20Algorithm.pdf)** | *Tech Stack:* `Python` `Subnetwork Allow-Lists` `Automation`
> **Objective:** Developed a Python algorithm to manage access control for a healthcare company's restricted subnetworks.
> 
> **Outcome:** Programmed a script that reads an allow list and a remove list, compares the IP addresses, identifies matches, and removes those IPs from the allow list to maintain updated access controls.
</details>

<details>
<summary><b>Enterprise File System Security & Linux Administration</b></summary>
<br>

*📁 Core Lab:* **[File System Permissions Assessment for Research Team](./managing-file-permissions-with-linux-commands/Managing%20File%20Permissions%20with%20Linux%20Commands.pdf)** | *Tech Stack:* `Linux CLI` `chmod` `chown` `Access Control`
> **Objective:** Managed file system permissions for a research team within a large organization.
> 
> **Outcome:** Reviewed existing file permissions against required authorizations, made necessary adjustments using Linux commands, and removed unauthorized access to protect sensitive information.
</details>

---

## 4. Governance, Risk, & Compliance (GRC)

<details>
<summary><b>Internal IT Audit & Risk Mitigation</b></summary>
<br>

*📁 Core Lab:* **[Internal IT Audit for Botium Toys](./security-audit/Security%20Audit%20-%20Performing%20Internal%20Audit.pdf)** | *Tech Stack:* `Compliance Checklist` `Internal IT Audit`
> **Objective:** Conducted an internal IT audit for a growing toy company to ensure compliance, secure operations, and identify risks.
> 
> **Outcome:** Reviewed scope, goals, and risk assessments to perform an internal audit with a compliance checklist, identified infrastructure vulnerabilities, and recommended mitigation strategies.
</details>

<details>
<summary><b>Public-Facing Infrastructure Vulnerability Assessment</b></summary>
<br>

*📁 Core Lab:* **[Vulnerability Assessment Report for a Small Business](./vulnerability-assessment/Vulnerability%20Assessment%20Report.pdf)** | *Tech Stack:* `Database Security` `Risk Evaluation` `Remediation Planning`
> **Objective:** Conducted a vulnerability assessment for an e-commerce company with a publicly accessible database server.
> 
> **Outcome:** Evaluated risks associated with the open server, identified security weaknesses, and authored a detailed report outlining the impacts alongside a remediation plan to secure the database server.
</details>

<details>
<summary><b>Threat Modeling & Architectural Risk Analysis</b></summary>
<br>

*📁 Core Lab:* **[PASTA Threat Model for Sneaker Company App](./threat-modeling-practice/Threat%20Modeling%20Practice%20-%20Applying%20the%20PASTA%20Threat%20Modeling%20Framework.pdf)** | *Tech Stack:* `PASTA Framework` `Threat Landscape Analysis` `Attack Simulation`
> **Objective:** Performed a threat model for a mobile app using the PASTA framework to assess security readiness before launch.
> 
> **Outcome:** Analyzed business objectives, technical scope, threat landscapes, and security requirements to simulate attack scenarios and establish security controls and mitigation strategies.
</details>

### Targeted Risk Analysis Matrices
The following assessments focus on specific organizational risk matrices, mapping data handling practices and evaluating asset vulnerabilities:

| Deliverable Portfolio Document | Target Organization & Context | Core Objective & Framework |
| :--- | :--- | :--- |
| 📄 [Data Risk Assessment](./data-risk-assessment/Data%20Risk%20Assessment%20-%20Determining%20Appropriate%20Data%20Handling%20Practices.pdf) | Educational Technology Company (Post-Breach) | Assessed post-incident data handling practices and recommended internal privacy and security improvements. |
| 📄 [Risk Assessment & Register](./risk-assessment/Risk%20Assessment%20-%20Risk%20Register.pdf) | Commercial Bank (Fictional) | Created a structured risk register evaluating threat likelihood and impact to optimize security mitigation resources. |
