# **MITRE ATT&CK Framework Analysis: APT Group Comparison**

>[!info]
>This assignment is done by **Tarun Sreenivasulu** for **Cyber Threat Hunting** Class in Spring 2025 at University at Albany, SUNY.
## **1. Introduction**  

Advanced Persistent Threat (APT) groups pose significant cybersecurity risks to organizations worldwide. This report analyzes and compares the attack techniques of **two well-known APT groups** using the **MITRE ATT&CK** framework. The objective is to identify their **tactics, techniques, and tools**, visualize them using **MITRE ATT&CK Navigator**, and assign a **scoring system** to evaluate the severity and frequency of their attack techniques.

---
<div style="page-break-after: always;"></div>


## **2. APT Group Identification**  

Based on research and provided hints, the APT groups analyzed in this report are:  
### **Group 1: APT28  G0007 (Fancy Bear)**  
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
<div style="page-break-after: always;"></div>


## **3. MITRE ATT&CK Navigator Analysis**  

The **MITRE ATT&CK Navigator** was used to visualize and analyze attack techniques for both groups:  
### Group 1 - APT28:
#### Screenshot:
![](Group_1%20(1).svg)
<div style="page-break-after: always;"></div>


### Group 2 - APT41:
![](Group_2%20(1).svg)
<div style="page-break-after: always;"></div>


### Combined a+b:
![](combined_group_final.svg)
<div style="page-break-after: always;"></div>


### **Key Observations**  
- **Common techniques**: Both groups use **reconnaissance, credential access, and impact techniques**.  
- **Differences**:  
  - ==**APT28**== is **espionage-focused** and targets **governments** and **defense** sectors.  
  - ==**APT41**== conducts **both espionage and financial attacks**, including **ransomware**.  

| **Aspect**             | **APT28 (Fancy Bear)**            | **APT41 (Winnti Group)**                 |
| ---------------------- | --------------------------------- | ---------------------------------------- |
| **Primary Objective**  | Cyber-espionage (state-sponsored) | Espionage + Financially motivated        |
| **Sponsoring Nation**  | Russia (GRU)                      | China (State-sponsored + Financial Gain) |
| **Initial Access**     | Phishing, public exploits         | Supply chain, stolen credentials         |
| **Credential Dumping** | Moderate usage                    | Heavy usage                              |
| **Lateral Movement**   | RDP, credential reuse             | Pass-the-hash, SSH abuse                 |
| **Impact Techniques**  | Network DoS (T1498)               | Ransomware (T1486)                       |

---
<div style="page-break-after: always;"></div>


## **4. Scoring Methodology**  

A scoring system was developed to **quantify the impact and severity** of attack techniques:  

|**Criteria**|**Description**|**Scale (1-5)**|
|---|---|---|
|**Impact**|How damaging is the technique?|1 (Low) - 5 (High)|
|**Ease of Execution**|How easily can an attacker execute it?|1 (Difficult) - 5 (Easy)|
|**Detection Difficulty**|How hard is it to detect?|1 (Easy) - 5 (Hard)|
|**Frequency**|How commonly is this technique used by APT groups?|1 (Rare) - 5 (Very Common)|
Final Score = **(Impact + Ease of Execution + Detection Difficulty + Frequency) ÷ 4**

The scoring is applied for both the groups on ATT&CK Navigator, refer the JSON attachments.
These scores were applied in **MITRE ATT&CK Navigator** to prioritize **high-risk techniques**.

---
<div style="page-break-after: always;"></div>


## **5. Importance of Understanding APT Groups**  

Studying APT tactics using **MITRE ATT&CK** improves **cybersecurity strategy** by:

🔹 **Threat Intelligence Mapping** – Organizations can predict and defend against likely attack vectors. 
🔹 **Incident Response Optimization** – Knowing common **APT techniques** helps in **faster mitigation**.  
🔹 **Security Control Enhancements** – Defensive measures can be tailored to **detect high-scoring techniques** (e.g., credential dumping).  
🔹 **Attack Surface Reduction** – Proactive patching and **user awareness training** can prevent phishing and initial access techniques.
🔹**Enhancing Cybersecurity Defenses**: Organizations can **proactively defend** against threats by understanding APT tactics.  

By leveraging the **MITRE ATT&CK framework**, security teams can **better anticipate, detect, and mitigate** APT attacks.

---

## **6. Conclusion**  

This analysis compared **APT28 and APT41**, highlighting their **techniques, similarities, and differences**. By using **MITRE ATT&CK Navigator**, a **scoring system** was applied to evaluate **the most impactful attack methods**. Understanding these tactics enables **stronger cyber defense measures**.

---

## **7. Deliverables**  

📎 **Attached Files:**  
- **PDF Report** (this document)  
- JSON Files (Group 1, Group 2, Combined groups)
- **Screenshots of MITRE ATT&CK Navigator SVG's**  

