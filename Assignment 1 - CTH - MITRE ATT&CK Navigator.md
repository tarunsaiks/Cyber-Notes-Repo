# **MITRE ATT&CK Framework Analysis: APT Group Comparison**

## **1. Introduction**  
Advanced Persistent Threat (APT) groups pose significant cybersecurity risks to organizations worldwide. This report analyzes and compares the attack techniques of **two well-known APT groups** using the **MITRE ATT&CK** framework. The objective is to identify their **tactics, techniques, and tools**, visualize them using **MITRE ATT&CK Navigator**, and assign a **scoring system** to evaluate the severity and frequency of their attack techniques.

---

## **2. APT Group Identification**  

Based on research and provided hints, the APT groups analyzed in this report are:  

### **Group 1: APT29 (Cozy Bear)**  
- **State-sponsored** cyber-espionage group linked to **Russia**.  
- Targets **government entities, military organizations, and the defense sector**.  
- **Common Techniques:**  
  - **Spear Phishing (T1566.001)** – Delivering malicious attachments or links.  
  - ==**Phishing for information (T1598)**== -  send phishing messages to elicit sensitive information that can be used during targeting
  - **Credential Dumping (T1003)** – Extracting stored credentials for lateral movement.  
  - **Exploiting Public-Facing Applications (T1190)** – Leveraging vulnerabilities in exposed systems.  
  - ==**Network Denial of Service (T1498)**== – Impacting service availability.  

### **Group 2: APT41 (Winnti Group)**  
- **Highly versatile** group conducting **espionage and financially motivated attacks**.  
- Known for **supply chain compromises, ransomware, and sophisticated malware**.  
- **Common Techniques:**  
  - **Supply Chain Compromise (T1195)** – Injecting malicious code into trusted software.  
  - **Ransomware Deployment (T1486)** – Encrypting victim data for extortion.  
  - ==**Search Victim-Owned Websites (T1596)**== – Reconnaissance for publicly available data.  
  - ==**Data Encrypted for Impact (T1486)**== – Causing financial and operational disruption.  

---

## **3. MITRE ATT&CK Navigator Analysis**  

The **MITRE ATT&CK Navigator** was used to visualize and analyze attack techniques for both groups:  
### Group 1 - APT28:
#### Screenshot:
![](Group_1.svg)

### Group 2 - APT41:
![](Group_2.svg)

### **Key Observations**  
- **Common techniques**: Both groups use **reconnaissance, credential access, and impact techniques**.  
- **Differences**:  
  - ==**APT29**== is **espionage-focused** and targets **governments** and **defense** sectors.  
  - ==**APT41**== conducts **both espionage and financial attacks**, including **ransomware**.  

---

## **4. Scoring Methodology**  

A scoring system was developed to **quantify the impact and severity** of attack techniques:  

| **Criteria** | **Description** | **Scale (1-5)** |
|-------------|----------------|----------------|
| **Impact** | How damaging is the technique? | 1 (Low) - 5 (High) |
| **Ease of Execution** | How easily can an attacker execute it? | 1 (Difficult) - 5 (Easy) |
| **Detection Difficulty** | How hard is it to detect? | 1 (Easy) - 5 (Hard) |

### Scoring for APT28:
|                                                                                                            |        |                   |                      |             |
| ---------------------------------------------------------------------------------------------------------- | ------ | ----------------- | -------------------- | ----------- |
| Attack Technique                                                                                           | Impact | Ease of Execution | Detection Difficulty | Score (1-5) |
| T1134.001 Access Token Manipulation: Token Impersonation/Theft1                                            | 4      | 3                 | 4                    | 4           |
| T1098.002 Account Manipulation: Additional Email Delegate Permissions1                                     | 4      | 3                 | 3                    | 3           |
| T1583.001 Acquire Infrastructure: Domains1                                                                 | 3      | 2                 | 2                    | 2           |
| T1583.003 Acquire Infrastructure: Virtual Private Server2                                                  | 3      | 2                 | 2                    | 2           |
| T1583.006 Acquire Infrastructure: Web Services2                                                            | 3      | 2                 | 2                    | 2           |
| T1595.002 Active Scanning: Vulnerability Scanning2                                                         | 2      | 3                 | 3                    | 3           |
| T1557.004 Adversary-in-the-Middle: Evil Twin2                                                              | 4      | 3                 | 4                    | 4           |
| T1071.001 Application Layer Protocol: Web Protocols3                                                       | 3      | 4                 | 3                    | 3           |
| T1071.003 Application Layer Protocol: Mail Protocols3                                                      | 3      | 4                 | 3                    | 3           |
| T1560 Archive Collected Data4                                                                              | 4      | 4                 | 3                    | 4           |
| T1560.001 Archive via Utility4                                                                             | 4      | 4                 | 3                    | 4           |
| T1119 Automated Collection4                                                                                | 4      | 3                 | 3                    | 3           |
| T1547.001 Boot or Logon Autostart Execution: Registry Run Keys / Startup Folder4                           | 3      | 3                 | 3                    | 3           |
| T1037.001 Boot or Logon Initialization Scripts: Logon Script (Windows)5                                    | 3      | 3                 | 3                    | 3           |
| T1110 Brute Force5                                                                                         | 4      | 2                 | 4                    | 3           |
| T1110.001 Password Guessing5                                                                               | 4      | 2                 | 4                    | 3           |
| T1110.003 Password Spraying6                                                                               | 4      | 2                 | 4                    | 3           |
| T1059.001 Command and Scripting Interpreter: PowerShell6                                                   | 4      | 4                 | 3                    | 4           |
| T1059.003 Command and Scripting Interpreter: Windows Command Shell7                                        | 4      | 4                 | 3                    | 4           |
| T1092 Communication Through Removable Media7                                                               | 3      | 3                 | 4                    | 3           |
| T1586.002 Compromise Accounts: Email Accounts7                                                             | 5      | 3                 | 4                    | 4           |
| T1584.008 Compromise Infrastructure: Network Devices8                                                      | 4      | 3                 | 4                    | 4           |
| T1213 Data from Information Repositories8                                                                  | 4      | 3                 | 3                    | 3           |
| T1213.002 Sharepoint8                                                                                      | 4      | 3                 | 3                    | 3           |
| T1005 Data from Local System8                                                                              | 4      | 3                 | 3                    | 3           |
| T1039 Data from Network Shared Drive9                                                                      | 4      | 3                 | 3                    | 3           |
| T1025 Data from Removable Media9                                                                           | 4      | 3                 | 4                    | 4           |
| T1001.001 Data Obfuscation: Junk Data9                                                                     | 2      | 3                 | 4                    | 3           |
| T1074.001 Data Staged: Local Data Staging10                                                                | 3      | 3                 | 3                    | 3           |
| T1074.002 Data Staged: Remote Data Staging10                                                               | 3      | 3                 | 3                    | 3           |
| T1030 Data Transfer Size Limits10                                                                          | 2      | 3                 | 3                    | 3           |
| T1140 Deobfuscate/Decode Files or Information10                                                            | 3      | 3                 | 3                    | 3           |
| T1189 Drive-by Compromise11                                                                                | 4      | 3                 | 4                    | 4           |
| T1114.002 Email Collection: Remote Email Collection11                                                      | 5      | 3                 | 4                    | 4           |
| T1573.001 Encrypted Channel: Symmetric Cryptography11                                                      | 3      | 3                 | 4                    | 3           |
| T1546.015 Event Triggered Execution: Component Object Model Hijacking12                                    | 4      | 3                 | 4                    | 4           |
| T1048.002 Exfiltration Over Alternative Protocol: Exfiltration Over Asymmetric Encrypted Non-C2 Protocol12 | 4      | 3                 | 4                    | 4           |
| T1567 Exfiltration Over Web Service12                                                                      | 4      | 3                 | 3                    | 3           |
| T1190 Exploit Public-Facing Application13                                                                  | 5      | 3                 | 4                    | 4           |
| T1203 Exploitation for Client Execution13                                                                  | 4      | 3                 | 4                    | 4           |
| T1211 Exploitation for Defense Evasion13                                                                   | 4      | 3                 | 4                    | 4           |
| T1068 Exploitation for Privilege Escalation14                                                              | 5      | 3                 | 4                    | 4           |
| T1210 Exploitation of Remote Services14                                                                    | 5      | 3                 | 4                    | 4           |
| T1133 External Remote Services14                                                                           | 3      | 3                 | 3                    | 3           |
| T1083 File and Directory Discovery15                                                                       | 3      | 4                 | 2                    | 3           |
| T1589.001 Gather Victim Identity Information: Credentials15                                                | 5      | 3                 | 4                    | 4           |
| T1564.001 Hide Artifacts: Hidden Files and Directories15                                                   | 2      | 4                 | 3                    | 3           |
| T1564.003 Hide Artifacts: Hidden Window15                                                                  | 2      | 4                 | 3                    | 3           |
| T1070.001 Indicator Removal: Clear Windows Event Logs16                                                    | 4      | 4                 | 4                    | 4           |
| T1070.004 Indicator Removal: File Deletion16                                                               | 4      | 4                 | 4                    | 4           |
| T1070.006 Indicator Removal: Timestomp16                                                                   | 3      | 4                 | 4                    | 4           |
| T1105 Ingress Tool Transfer16                                                                              | 3      | 4                 | 3                    | 3           |
| T1056.001 Input Capture: Keylogging17                                                                      | 5      | 3                 | 4                    | 4           |
| T1559.002 Inter-Process Communication: Dynamic Data Exchange17                                             | 3      | 3                 | 3                    | 3           |
| T1036 Masquerading17                                                                                       | 2      | 4                 | 3                    | 3           |
| T1036.005 Match Legitimate Name or Location18                                                              | 2      | 4                 | 3                    | 3           |
| T1498 Network Denial of Service18                                                                          | 4      | 3                 | 3                    | 3           |
| T1040 Network Sniffing18                                                                                   | 4      | 3                 | 4                    | 4           |
| T1027.013 Obfuscated Files or Information: Encrypted/Encoded File18                                        | 3      | 3                 | 4                    | 3           |
| T1588.002 Obtain Capabilities: Tool19                                                                      | 3      | 4                 | 3                    | 3           |
| T1137.002 Office Application Startup: Office Test19                                                        | 3      | 3                 | 4                    | 3           |
| T1003 OS Credential Dumping20                                                                              | 5      | 3                 | 4                    | 4           |
| T1003.001 LSASS Memory20                                                                                   | 5      | 3                 | 4                    | 4           |
| T1003.003 NTDS20                                                                                           | 5      | 3                 | 4                    | 4           |
| T1120 Peripheral Device Discovery21                                                                        | 2      | 3                 | 3                    | 3           |
| T1566.001 Phishing: Spearphishing Attachment21                                                             | 4      | 3                 | 3                    | 3           |
| T1598 Phishing for Information21                                                                           | 4      | 3                 | 3                    | 3           |
| T1598.003 Spearphishing Link21                                                                             | 4      | 3                 | 3                    | 3           |
| T1542.003 Pre-OS Boot: Bootkit22                                                                           | 5      | 2                 | 5                    | 4           |
| T1057 Process Discovery22                                                                                  | 2      | 4                 | 2                    | 2           |
| T1090.002 Proxy: External Proxy22                                                                          | 3      | 3                 | 3                    | 3           |
| T1090.003 Proxy: Multi-hop Proxy23                                                                         | 3      | 3                 | 4                    | 3           |
| T1021.002 Remote Services: SMB/Windows Admin Shares23                                                      | 4      | 3                 | 3                    | 3           |
| T1091 Replication Through Removable Media23                                                                | 3      | 3                 | 4                    | 3           |
| T1014 Rootkit23                                                                                            | 5      | 2                 | 5                    | 4           |
| T1113 Screen Capture24                                                                                     | 4      | 4                 | 3                    | 4           |
| T1505.003 Server Software Component: Web Shell24                                                           | 4      | 3                 | 4                    | 4           |
| T1528 Steal Application Access Token24                                                                     | 5      | 3                 | 4                    | 4           |
| T1218.011 System Binary Proxy Execution: Rundll3225                                                        | 3      | 4                 | 3                    | 3           |
| T1221 Template Injection25                                                                                 | 4      | 3                 | 4                    | 4           |
| T1199 Trusted Relationship26                                                                               | 5      | 2                 | 4                    | 4           |
| T1550.001 Use Alternate Authentication Material: Application Access Token26                                | 5      | 3                 | 4                    | 4           |
| T1550.002 Use Alternate Authentication Material: Pass the Hash26                                           | 4      | 3                 | 4                    | 4           |
| T1204.001 User Execution: Malicious Link27                                                                 | 4      | 4                 | 3                    | 4           |
| T1204.002 User Execution: Malicious File27                                                                 | 4      | 4                 | 3                    | 4           |
| T1078 Valid Accounts27                                                                                     | 5      | 3                 | 4                    | 4           |
| T1078.004 Cloud Accounts28                                                                                 | 5      | 3                 | 4                    | 4           |
| T1102.002 Web Service: Bidirectional Communication28                                                       | 3      | 3                 | 3                    | 3           |
### **Scoring Example**  
| **Technique**                         | **Impact** | **Ease of Execution** | **Detection Difficulty** | **Total Score** |
| ------------------------------------- | ---------- | --------------------- | ------------------------ | --------------- |
| Spear Phishing (T1566.001)            | 5          | 4                     | 4                        | 13              |
| Credential Dumping (T1003)            | 4          | 3                     | 5                        | 12              |
| Exploiting Public-Facing Apps (T1190) | 5          | 5                     | 3                        | 13              |
| Ransomware (T1486)                    | 5          | 4                     | 5                        | 14              |
|                                       |            |                       |                          |                 |

These scores were applied in **MITRE ATT&CK Navigator** to prioritize **high-risk techniques**.

---

## **5. Importance of Understanding APT Groups**  

- **Enhancing Cybersecurity Defenses**: Organizations can **proactively defend** against threats by understanding APT tactics.  
- **Threat Intelligence Application**: Security teams can **map adversary behavior** to MITRE ATT&CK to **improve detection** and threat hunting strategies to remediate.  
- **Incident Response & Mitigation**: Knowing **common techniques** helps in **building resilient defense strategies**.  

By leveraging the **MITRE ATT&CK framework**, security teams can **better anticipate, detect, and mitigate** APT attacks.

---

## **6. Conclusion**  

This analysis compared **APT29 and APT41**, highlighting their **techniques, similarities, and differences**. By using **MITRE ATT&CK Navigator**, a **scoring system** was applied to evaluate **the most impactful attack methods**. Understanding these tactics enables **stronger cyber defense measures**.

---

## **7. Deliverables**  

📎 **Attached Files:**  
- **PDF Report** (this document)  
- **MITRE ATT&CK Navigator Layer (JSON file)**  
- **Screenshots of MITRE ATT&CK Navigator Merged Layer**  

📅 **Submission Deadline:** **February 25, 2025**  
