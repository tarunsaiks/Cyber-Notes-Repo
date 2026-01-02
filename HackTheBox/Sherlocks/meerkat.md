
# Sherlock Analysis Report: Meerkat

## Scenario

As a security provider for Forela, an analysis was conducted on exported [PCAP](https://fidelissecurity.com/threatgeek/network-security/pcap-analysis/) and log data to confirm a potential compromise of their business management platform.

---

## Phase 1: Vulnerability Identification

- **Application Identified**: The compromised server was running **BonitaSoft**.
	- **How?** : `jq '.[].alert.signature' meerkat-alerts.json | sort | uniq`
- **Attack Classification**: The attacker utilized a subset of the brute forcing attack category known as **Credential Stuffing**.
- **Vulnerability Exploited**: The specific vulnerability identified was **CVE-2022-25237**.
- **Bypass Technique**: To bypass the authorization filter, the attacker appended the string `i18ntranslation` to the API URL path.

---

## Phase 2: Exploit Analysis

- **Credential Volume**: A total of **56** unique combinations of usernames and passwords were used during the [Credential Stuffing](https://www.google.com/search?q=https://www.f5.com/glossary/credential-stuffing) attack.
    
- **Successful Compromise**: The successful login was achieved using the credentials `seb.broom@forela.co.uk:g0vernm3nt`.
    

---

## Phase 3: Persistence and Exfiltration

- **External Infrastructure**: The attacker utilized the text-sharing site **pastes.io** during the exploit.
    
- **Malicious Payload**: A public key file named **hffgra4unv** was used to gain persistence on the host.
    
- **System Modification**: The attacker modified the **/home/ubuntu/.ssh/authorized_keys** file to maintain access.
    
- **MITRE ATT&CK Mapping**: This persistence mechanism is categorized under MITRE technique ID **T1098.004** ([SSH Authorized Keys](https://attack.mitre.org/techniques/T1098/004/)).
    

---

Would you like me to help you format this into a professional **Incident Response Report** template that you can use for your records?