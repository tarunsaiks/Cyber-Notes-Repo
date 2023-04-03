## What are security frameworks?

Security frameworks are the processes that define policies and procedures organizations should follow to establish and manage security controls.

They are the blueprints for identifying managing the risks they may face and the weakness in place that may lead to an attack.

### NIST

NIST (National Institute of Standards and Technology) developed a CSF (Cybersecurity Framework) it provides a detailed guidance for organizations to manage and cybersecurity risk.

The framework focuses on 5 essential functions:
+ ### Identify
+ ### Protect
+ ### Detect
+ ### Respond
+ ### Recover

### ISO 27000

ISO develops a series of frameworks for 27001 and 27002 standards are known for cybersecurity and outline the requirements and procedures for creating, implmenting and managing an Information Security Management System (ISMS).

Read more about ISO 27001 from Skillfront course here ![[ISO 27001]]

#### MITRE ATT&K

 Identifying adversary plans of attack can be challenging to embark on blindly which can be understood through behaivours, methods, tools and strategies established for an attack. Commonly known as TTP (Tactics, Techniques and Procedures)

![[Endpoint Detection and Response#**MITTRE ATT&CK Framework**]]
 
### Cyber Kill Chain

Kill Chain : Describes the structure of an attack and conists of target information, decision and order to attack the target and finally target destruction.

There are seven stages in Cyber Kill Chain
1. Recon
2. Weaponization
3. Delivery
4. Exploitation
5. Installation
6. Command & Control
7. Actions on Objectives

### Unified Kill Chain

It is combination of MITRE ATT&K and Cyber Kill Chain frameworks Published by Paul Pols in 2017 (reviewed in 2022).

UKC provides a model to defend against cyber attacks from adversaries. It offers security teams a blueprint for analysing and comparing threat intelligence concerning adversial mode of working.

UKC describes 18 phases of attack based on TTP's. Individual phases can be combined to form overarching goals like 
+ Gaining initial foothold in a targeted network
+ Navigating through network to expand access.
+ Performing actions on critical assets.

## 3 Cycles an attacker would use (In, Through, Out)

### Cycle 1 : In

Critical steps an attacker would follow to gain access to a system or networked environment are:
1. **Reconaissance** - Performs research on target using publicly available.
2. **Weaponization** = Setting up the needed infrastructure to host c2 (Command and Control) centre
3. **Delivery** - Payloads are malicious instruments delivered to target through email, phising and supply chain attacks.
4. **Social Engineering** - Tricking the target into performing untrusted and unsafe action against the payload they just delivered
5. **Exploitation** - If attacker finds an existing vulnerability, a software or hardware weakness, in the network assets, they may use this to trigger their payload.
6. **Persistence** - The attacker will leave behind a fallback presence on network to make sure they have a point of access to the target.
7. **Defence Evasion** - attacker remains anon throughout their exploits by disabling and avoiding any security defence mechanisms enabled, including deleting the evidence of their presence.
8. **Command & Control** - Remember the infrastructure that the attacker prepared? A communication channel between the compromised system and the attacker’s infrastructure is established across the internet.

#### CYCLE 2: Through

Under this phase, attackers will be interested in gaining more access and privileges to assets within the network.

The attacker may repeat this phase until the desired access is obtained.

-   ![Yeti gathering gifts after gaining access to the warehouse.](https://tryhackme-images.s3.amazonaws.com/user-uploads/5fc2847e1bbebc03aa89fbf2/room-content/e39706bbb1ce71dce5da3b93343722f5.png)**
    
    **Pivoting**: Remember the system that the attacker may use for persistence? This system will become the attack launchpad for other systems in the network.
    
    **
-   **Discovery**: The attacker will seek to gather as much information about the compromised system, such as available users and data. Alternatively, they may remotely discover vulnerabilities and assets within the network. This opens the way for the next phase.
-   **Privilege Escalation**: Restricted access prevents the attacker from executing their mission. Therefore, they will seek higher privileges on the compromised systems by exploiting identified vulnerabilities or misconfigurations.
-   **Execution**: With elevated privileges, malicious code may be downloaded and executed to extract sensitive information or cause further havoc on the system.
-   **Credential Access**: Part of the extracted sensitive information would include login credentials stored in the hard disk or memory. This provides the attacker with more firepower for their attacks.
-   **Lateral Movement**: Using the extracted credentials, the attacker may move around different systems or data storages within the network, for example, within a single department.

**NOTE**: A key element that one may think is missing is Access. This is not formally covered as a phase of the UKC, as it overlaps with other phases across the different levels, leading to the adversary achieving their goals for an attack.

#### CYCLE 3: Out

The Confidentiality, Integrity and Availability (CIA) of assets or services are compromised during this phase. Money, fame or sabotage will drive attackers to undertake their reasons for executing their attacks, cause as much damage as possible and disappear without being detected.

![Yeti leaving Santa's warehouse happy with his loot.](https://tryhackme-images.s3.amazonaws.com/user-uploads/5fc2847e1bbebc03aa89fbf2/room-content/e2e5af4067e65918c2ce6827143cecb6.png)-   **Collection**: After finding the jackpot of data and information, the attacker will seek to aggregate all they need. By doing so, the assets’ confidentiality would be compromised entirely, especially when dealing with trade secrets and financial or personally identifiable information (PII) that is to be secured.
-   **Exfiltration**: The attacker must get his loot out of the network. Various techniques may be used to ensure they have achieved their objectives without triggering suspicion.
-   **Impact**: When compromising the availability or integrity of an asset or information, the attacker will use all the acquired privileges to manipulate, interrupt and sabotage. Imagine the reputation, financial and social damage an organisation would have to recover from.
-   **Objectives**: Attackers may have other goals to achieve that may affect the social or technical landscape that their targets operate within. Defining and understanding these objectives tends to help security teams familiarise themselves with adversarial attack tools and conduct risk assessments to defend their assets.