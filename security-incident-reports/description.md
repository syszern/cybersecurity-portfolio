## Security Incident Reports
This section highlights a collection of projects dedicated to identifying, analyzing, and addressing cybersecurity incidents. The primary objective of these projects is to enhance the security posture of the affected systems through thorough investigation, root cause analysis, and the implementation of preventive measures.

## Analyzing Network Attacks for Travel Agency
**Background:** A security analyst at a travel agency received an automated alert indicating an issue with the web server, which employees use to access vacation package information. The alert suggested a potential disruption in service, requiring immediate investigation.

**Objective:**
The goal is to investigate the security event, identify the nature of the attack, document the incident thoroughly, and recommend preventive measures to avoid similar future occurrences.

**Key Tasks:**
1. **Investigate the Security Event:**
Upon attempting to access the website, the analyst encountered a connection timeout. A packet sniffer was used to capture data packets, revealing an unusually high volume of TCP SYN requests from an unfamiliar IP address.

2. **Identify the Attack:**
The web server was overwhelmed by a flood of incoming traffic, indicating a potential SYN flood attack, commonly associated with a Denial of Service (DoS) attack aimed at exhausting the server's resources.

3. **Immediate Response:**
The web server was temporarily taken offline to recover, and the company’s firewall was configured to block the offending IP address, mitigating the immediate threat and restoring service.

4. **Alert Management:**
The manager was promptly notified about the issue, and next steps were discussed to prevent recurrence. The attack type and its impact on the server were documented for senior management to understand and address the risks.

**Outcome:**
The incident was resolved by identifying the attack, taking immediate corrective action, and implementing a more robust defense strategy to prevent future attacks. The travel agency’s website security was reinforced, enhancing its ability to handle such threats in the future.

## Network Traffic Analysis for Cybersecurity Incident

**Objective:**
  - Analyze the DNS & HTTP traffic log to identify a network protocol.
  - Document the cybersecurity incident.
  - Recommend one security measure to prevent brute force attacks in the future.

**Tasks:**
1. **Analyze DNS & HTTP Traffic:** Review the traffic log to identify a network protocol involved in the incident.
   
2. **Document the Incident:** Record the details of the cybersecurity incident, including the identified network protocol.
   
3. **Recommend a Security Measure:** Propose one security measure to implement to prevent future brute force attacks, thereby improving the organization’s security posture.

**Outcome:** Enhance the organization's security posture by identifying the network protocol involved in the incident, documenting the event, and recommending preventive measures to mitigate future brute force attacks.

## Applying OS Hardening Techniques
**Background:** A cybersecurity analyst working for a company that hosts the cooking website *yummyrecipesforme.com* is tasked with investigating a security issue experienced by visitors when loading the main webpage. Malicious actors may exploit network protocols to invade private networks, highlighting the importance of identifying and protecting against such threats.

**Objective:** Investigate the security event, identify the network protocols involved, document the incident, and recommend a security measure to prevent similar issues in the future.

**Tasks:**

1. **Investigate the Security Event:**
    - Use a tcpdump log to analyze the network traffic.
    - Identify the network protocols used to establish the connection between the user and the website.

2. **Document the Incident:** Record the details of the cybersecurity incident, including the network protocols involved and how they were exploited.

3. **Recommend a Security Measure:** Propose one actionable security measure to implement, ensuring protection against similar security problems in the future.

**Outcome:** Enhance the security of *yummyrecipesforme.com* by identifying and addressing the network protocol vulnerabilities, documenting the incident, and implementing a preventive solution to protect against future threats.
