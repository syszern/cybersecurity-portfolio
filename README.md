# Cybersecurity Portfolio

This repository contains a collection of portfolio documents showcasing my work and skills in cybersecurity, completed during the Google Cybersecurity Professional Certificate program.

## Table of Contents
- [Data Risk Assessment](#data-risk-assessment)
- [Risk Assessment](#risk-assessment)
- [Security Incident Reports](#security-incident-reports)
- [Access Control Assessment](#access-control-assessment)
- [Threat Modeling Practice](#threat-modeling-practice)
- [Playbook Response to Phishing Incident](#playbook-response-to-phishing-incident)
- [Vulnerability Assessment Report](#vulnerability-assessment-report)
- [NIST CSF for Security Incident Response](#nist-csf-for-security-incident-response)
- [Security Audit (Internal Audit)](#security-audit-internal-audit)
- [Wireshark Packet Data Inspection for Website Traffic](#wireshark-packet-data-inspection-for-website-traffic)
- [File Update through a Python Algorithm](#file-update-through-a-python-algorithm)
- [Managing File Permissions with Linux Commands](#managing-file-permissions-with-linux-commands)
  

## Data Risk Assessment
### Data Risk Assessment for Educational Technology Company
Background: An educational technology company developed an application to help teachers automatically grade assignments, handling a wide range of data from academic institutions, instructors, parents, and students. The team was alerted to a data leak of internal business plans on social media, caused by an employee accidentally sharing confidential documents with an external business partner. An audit is underway to prevent similar incidents in the future.

Objective:
- Determine whether effective data handling processes are being implemented to protect information privacy.
- Analyze the data leak incident and propose measures to improve information privacy and data handling.

Tasks:

1. **Evaluate the Incident:** Review details about the data leak incident, including how the principle of least privilege was not observed.

2. **Review Data Handling Controls:** Assess the current controls in place to prevent data leaks and determine their effectiveness.

3. **Identify Improvements:** Propose ways to improve information privacy and data handling processes at the company.

4. **Justify Recommendations:** Explain why the proposed recommendations will enhance data handling and security at the company.

Outcome: Strengthen the company's data handling processes and information privacy by analyzing the incident, reviewing current controls, and implementing effective measures to prevent future data leaks.

## Risk Assessment
### Risk Assessment for Commercial Bank
Background: A new cybersecurity team at a commercial bank is conducting a risk assessment of the bank's current operational environment. The team is creating a risk register to focus on securing the most vulnerable risks.

Objective: Perform a risk assessment by evaluating vulnerabilities that threaten business operations and prioritize resources based on the risk scores assigned to each vulnerability.

Tasks:

1. **Evaluate Risks:**
    - Review the set of risks recorded in the risk register.
    - Determine the likelihood of each risk occurring.
    - Assess the potential impact of each risk on the bank.

2. **Calculate Risk Scores:**
    - Assign a score to each risk based on its likelihood and severity.
    - Compare the scores across all risks to prioritize attention for each risk.

Process:

1. **Create a Risk Register:** Maintain a central record of potential risks to the organization's assets, information systems, and data.

2. **Assess Likelihood and Impact:** Evaluate how likely each risk is to occur and how severely it may impact the bank.

3. **Prioritize Risks:** Use the risk scores to determine how to allocate resources and focus on securing the most vulnerable risks.

Outcome: Improve the bank's security posture by identifying, evaluating, and prioritizing risks, allowing the cybersecurity team to effectively allocate resources and mitigate potential threats.

## Security Incident Reports
### Security Incident Analysis for YummyRecipesForMe.com
- Background: Visitors to the cooking website yummyrecipesforme.com experienced a security issue when loading the main webpage. The cybersecurity analyst's role is to investigate, identify, document, and recommend a solution to the security problem.

- Objective: Investigate the security event, identify the affected network protocols, and recommend a preventive security measure.

- Tasks:
1. **Investigate the Security Event:** Review a tcpdump log to analyze the network traffic and identify the network protocols used to establish the connection between the user and the website.

2. **Identify Network Protocols:** Understand the communication rules and standards used by networked devices to transmit data. Recognize how malicious actors can exploit these protocols to invade and attack private networks.

3. **Document the Incident:** Record the details of what occurred during the security incident.

4. **Recommend a Security Measure:** Propose one security measure to implement to prevent similar security problems in the future.

Outcome: Enhance the security of yummyrecipesforme.comby identifying and addressing the security issue, documenting the incident, and implementing preventive measures to protect against future attacks.

### DNS & HTTP Traffic Analysis for Cybersecurity Incident

Objective:
Analyze the DNS & HTTP traffic log to identify a network protocol.
Document the cybersecurity incident.
Recommend one security measure to prevent brute force attacks in the future.

Tasks:
1. **Analyze DNS & HTTP Traffic:** Review the traffic log to identify a network protocol involved in the incident.

2. **Document the Incident:** Record the details of the cybersecurity incident, including the identified network protocol.

3. **Recommend a Security Measure:** Propose one security measure to implement to prevent future brute force attacks, thereby improving the organization’s security posture.

Outcome: Enhance the organization's security posture by identifying the network protocol involved in the incident, documenting the event, and recommending preventive measures to mitigate future brute force attacks.

### Network Hardening for Social Media Organization
Background: A social media organization recently experienced a major data breach due to undetected vulnerabilities. The goal is to address the breach by implementing network hardening tools and methods to protect the organization’s overall security.

Objective:
Identify common network hardening tools to protect the organization’s security.
Select a specific vulnerability and propose different network hardening methods.
Explain the effectiveness of the chosen methods and tools in managing the vulnerability and preventing future breaches.

Tasks:
1. **Identify Network Hardening Tools:** Recognize common tools such as port filtering, network access privileges, and encryption over networks.

2. **Select Specific Vulnerability**: Choose a particular vulnerability within the company’s network.

3. **Propose Network Hardening Methods:** Recommend various methods to address the selected vulnerability.

4. **Explain Effectiveness:** Describe how the chosen methods and tools will manage the vulnerability and prevent potential breaches in the future.

Outcome: Enhance the organization's security posture by implementing effective network hardening tools and methods, thereby mitigating vulnerabilities and protecting against future data breaches.

### Security Incident Response: Analyzing Network Attacks for Travel Agency
Background: A security analyst at a travel agency, which advertises sales and promotions on the company's website, received an automated alert from the monitoring system indicating a problem with the web server. Employees regularly access the company's sales webpage to search for vacation packages for their customers.

Objective: Investigate the security event, identify the type of attack, document the incident, and recommend steps to prevent future occurrences.

Tasks:

1. **Investigate the Security Event:** Attempt to visit the company’s website and observe the connection timeout error message. Use a packet sniffer to capture data packets in transit to and from the web server. Identify a large number of TCP SYN requests coming from an unfamiliar IP address.

2. **Identify the Attack:** Determine that the web server is overwhelmed by the volume of incoming traffic, indicating a potential attack by a malicious actor.

3. **Immediate Response:** Take the server offline temporarily to allow it to recover and return to normal operating status.
Configure the company’s firewall to block the IP address sending the abnormal number of SYN requests.

4. **Alert Management:** Quickly alert the manager about the problem and discuss the next steps to stop the attacker and prevent future incidents.
Prepare to explain to the boss the type of attack discovered and its impact on the web server and employees.

Outcome: Enhance the security of the travel agency’s website by identifying and addressing the attack, documenting the incident, and implementing preventive measures to protect against future attacks.

## Access Control Assessment
### Access Control Assessment for Growing Business
Background: A newly hired cybersecurity professional at a growing business is tasked with assessing the access controls used by the business. Recently, a deposit was made from the business to an unknown bank account, which was fortunately stopped by the finance manager. The business owner has requested an investigation to prevent future incidents.

Objective: Analyze the current access control process, identify issues, and recommend improvements to enhance security practices and prevent similar incidents.

Tasks:
1. **Review the Access Log:** Examine the access log of the incident to understand what happened.

2. **Identify Threat Actor:** Take notes to help identify a possible threat actor involved in the incident.

3. **Spot Access Control Issues:** Identify issues with the access controls that were exploited by the user.

4. **Recommend Mitigations:** Propose mitigations to improve the business's access controls and reduce the likelihood of similar incidents reoccurring.

Outcome: Enhance the security of the growing business by analyzing the incident, identifying access control issues, and implementing effective mitigations to prevent future security breaches.

## Threat Modeling Practice
### PASTA Threat Model for Sneaker Company App
Background: A company for sneaker enthusiasts and collectors is preparing to launch a mobile app that facilitates buying and selling shoes. The security team, including the cybersecurity analyst, needs to determine if the new app is safe to launch.

Objective: Perform a threat model of the application using the Process of Attack Simulation and Threat Analysis (PASTA) framework to identify security requirements for the new sneaker company app.

Tasks:
1. **Understand Business Objectives:**  Identify the business goals and objectives for the new sneaker company app.

2. **Define the Technical Scope:** Outline the app's architecture, components, and data flow.

3. **Analyze the Threat Landscape:** Identify potential threats and vulnerabilities that could impact the app.

4. **Evaluate Security Requirements:** Determine the security requirements needed to protect the app from identified threats.

5. **Analyze Attack Vectors:** Simulate possible attack scenarios and assess the impact on the app.

6. **Assess Risk:** Evaluate the likelihood and impact of potential attacks and prioritize mitigation strategies.

7. **Plan Security Controls:** Recommend security controls and measures to protect the app and ensure it meets security requirements.

Outcome: Ensure the new sneaker company app is secure by identifying and mitigating potential threats through the PASTA framework, ultimately supporting a safe and successful launch.

## Playbook Response to Phishing Incident
### Responding to a Phishing Incident for Financial Services Company
Background: A level-one security operations center (SOC) analyst at a financial services company received a phishing alert about a suspicious file downloaded on an employee's computer. The email attachment file's hash has been verified as malicious. The analyst must follow the organization's process to complete the investigation and resolve the alert.

Objective: Investigate the phishing incident, follow the organization's security policies and procedures, and update the alert ticket with findings about the incident.

Tasks:
1. **Investigate the Phishing Incident:**
    - Follow the organization's security policies and procedures for responding to phishing alerts.
    - Use the playbook, including the flowchart and written instructions, to guide the investigation.

2. **Resolve the Alert:**
    - Complete the investigation according to the steps outlined in the playbook.
    - Take necessary actions to mitigate the threat and secure the affected system.

3. **Update the Alert Ticket:**
    - Document the findings of the investigation in the alert ticket.
    - Include details about the malicious file hash, the actions taken, and the resolution of the incident.

Outcome: Effectively respond to the phishing incident by following the organization's security policies and procedures, completing the investigation, and updating the alert ticket with detailed findings to enhance the company's security posture.

## Vulnerability Assessment Report
### Vulnerability Assessment for E-commerce Company
Background: A newly hired cybersecurity analyst for an e-commerce company is tasked with conducting a vulnerability assessment. The company stores information on a remote database server, which has been open to the public since the company's launch three years ago. Employees working remotely query data from the server to find potential customers.

Objective:
Evaluate the risks associated with the vulnerable information system.
Outline a remediation plan to secure the database server.

Tasks:
1. **Conduct Vulnerability Assessment:** Review the current security systems and identify vulnerabilities in the database server. Assess the risks associated with keeping the database server open to the public.

2. **Communicate Potential Risks:** Create a written report explaining how the vulnerable server poses a risk to business operations. Highlight the potential consequences of maintaining the current security posture.

3. **Outline Remediation Plan:** Propose measures to secure the database server and prevent unauthorized access. Recommend best practices for maintaining the security of remote database servers.

Outcome: Enhance the security of the e-commerce company by identifying vulnerabilities, communicating potential risks to decision-makers, and implementing a remediation plan to protect the database server.

## NIST CSF for Security Incident Response
### Incident Report and Network Security Plan for Multimedia Company
Background: A cybersecurity analyst working for a multimedia company that offers web design services, graphic design, and social media marketing solutions to small businesses recently encountered a DDoS attack. The attack compromised the internal network for two hours until it was resolved. During the attack, the organization’s network services stopped responding due to an incoming flood of ICMP packets, preventing normal internal network traffic from accessing resources.

Objective:
  - Analyze the network incident using the National Institute of Standards and   Technology's Cybersecurity Framework (NIST CSF).
  - Create an incident report detailing the DDoS attack and the steps taken to resolve it.
  - Develop a plan to improve the company's network security and prevent future incidents.

Tasks:
1. **Analyze the Situation:** Review the DDoS attack and its impact on the network.
Investigate the security event and identify the vulnerability that allowed the attack.

2. **Create Incident Report:** Document the details of the DDoS attack, including the incoming flood of ICMP packets and the network's response. Record the actions taken by the incident management team to block ICMP packets, take non-critical services offline, and restore critical services.

3. **Develop Network Security Plan:** Implement new firewall rules to limit the rate of incoming ICMP packets.
Verify the source IP addresses on the firewall to check for spoofed IP addresses on incoming ICMP packets.
Deploy network monitoring software to detect abnormal traffic patterns.
Use an IDS/IPS system to filter out ICMP traffic based on suspicious characteristics.

4. **Follow NIST CSF Steps:**
  - **Identify:** Conduct regular audits of internal networks, systems, devices, and access privileges to identify potential security gaps.
  - **Protect:** Implement policies, procedures, training, and tools to mitigate cybersecurity threats.
  - **Detect:** Improve monitoring capabilities to increase the speed and efficiency of detecting potential security incidents.
  - **Respond:** Contain, neutralize, and analyze security incidents; implement improvements to the security process.
  - **Recover:** Restore affected systems to normal operation and recover systems data and/or assets affected by the incident.

Outcome: Enhance the company's network security by documenting the incident, implementing preventive measures, and following the NIST Cybersecurity Framework (CSF) to protect against future attacks.

## Security Audit (Internal Audit)
### Internal IT Audit for Botium Toys

Background: Botium Toys, a U.S.-based toy company with a growing online presence, is facing increased IT demands.

Objective: Conduct an internal IT audit to ensure compliance, secure operations, and support growth by identifying and mitigating risks and vulnerabilities.

Scope and Goals:
- Implement the NIST Cybersecurity Framework (CSF).
- Establish audit scope and goals.
- List IT-managed assets.
- Complete a risk assessment.

Tasks:
1. Review the IT manager’s scope, goals, and risk assessment report.
2. Perform an internal audit using a controls and compliance checklist.
3. Identify vulnerabilities in the company's infrastructure.
4. Recommend mitigation strategies to improve security posture.

Outcome: Enhance Botium Toys' security, ensure compliance, and support its long-term growth by addressing potential risks and vulnerabilities.

## Wireshark Packet Data Inspection for Website Traffic
### Analyzing Sample Packet Capture and Filtering Network Traffic Data

Background: This lab activity involves examining a sample packet capture file to investigate traffic to a website.

Objective: Analyze a network packet capture file to identify the source and destination IP addresses, examine the protocols used during the connection, and analyze data packets to identify the type of information sent and received.

Tasks:
1. **Analyze Packet Capture File:** Use Wireshark to examine the sample packet capture file and filter the network traffic data.

2. **Identify IP Addresses:** Filter the data to identify the source and destination IP addresses involved in the web browsing session.

3. **Examine Protocols:** Analyze the protocols used when the user makes the connection to the website.

4. **Analyze Data Packets:** Identify the type of information sent and received by the systems when the network data is captured.

Outcome: Enhance the ability to efficiently filter and analyze network traffic using Wireshark, which is an essential skill for a security analyst. The activity will improve understanding of network protocols and data packet analysis to investigate website traffic.

## File Update through a Python Algorithm
### Access Control Update for Health Care Company

Background: A security professional at a health care company is responsible for regularly updating a file that identifies employees who can access restricted content based on their IP addresses. The company maintains an allow list for IP addresses permitted to sign into the restricted subnetwork and a remove list for IP addresses that should be removed from the allow list.

Objective: Create an algorithm using Python code to check whether the allow list contains any IP addresses identified on the remove list and remove those IP addresses from the allow list file.

Tasks:
1. **Check for IP Addresses:** Create a Python algorithm to compare the allow list and the remove list.

2. **Update Allow List:** Remove any IP addresses from the allow list that are identified on the remove list.

Steps:
1. **Read the Allow List and Remove List:** Load the allow list and remove list from their respective files.

2. **Compare IP Addresses:** Check each IP address in the allow list against the remove list.

3. **Remove Identified IP Addresses:** Remove any IP addresses found in the remove list from the allow list.

4. **Save the Updated Allow List:** Write the updated allow list back to the file.

Outcome: Ensure that the allow list for the restricted subnetwork is updated by removing any unauthorized IP addresses, thereby maintaining the security and integrity of the health care company's access controls.

## Managing File Permissions with Linux Commands
### File System Permissions Assessment for Research Team
Background: A security professional at a large organization mainly works with the research team. Part of the professional's job is to ensure that users on this team are authorized with the appropriate permissions, which helps keep the system secure.

Objective:
- Examine existing permissions on the file system.
- Determine if the permissions match the authorization that should be given.
- Modify the permissions to authorize the appropriate users and remove any unauthorized access.

Tasks:
1. **Examine Permissions:** Review the current permissions on the file system to understand who has access to what resources.
2. **Match Authorization:** Determine if the current permissions align with the authorization that should be given to users on the research team.
3. **Modify Permissions:**
    - Adjust the file system permissions to authorize the appropriate users.
    - Remove any unauthorized access to ensure the system remains secure.

Outcome: Enhance the security of the organization's file system by ensuring that permissions are appropriately assigned to users on the research team, thereby maintaining secure access to sensitive information.
