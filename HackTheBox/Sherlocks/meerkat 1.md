
# Sherlock Analysis Report: Meerkat

## Scenario

As a security provider for Forela, an analysis was conducted on exported [PCAP](https://fidelissecurity.com/threatgeek/network-security/pcap-analysis/) and log data to confirm a potential compromise of their business management platform.

---

## Phase 1: Vulnerability Identification

- **Application Identified**: The compromised server was running **BonitaSoft**.
	- **How?** : `jq '.[].alert.signature' meerkat-alerts.json | sort | uniq`
- **Attack Classification**: The attacker utilized a subset of the brute forcing attack category known as **Credential Stuffing**.
- **Vulnerability Exploited**: 
	- To find CVE's from the alert JSON, use `jq`.
	- The specific vulnerability identified was **CVE-2022-25237**
```
jq .[].alert.signature meerkat-alerts.json | grep -o "CVE-[0-9-]*"
```
- **List Requests made by Attacker**: To get list of the requests, we can either use Statistics --> HTTP --> Requests or fetch them from `.pcap` using `tshark`
```
tshark -r meerkat.pcap -T json | jq -r '.. | ."http.request.uri"? // empty' | sort -u
```
- **Bypass Technique**: To bypass the authorization filter, the attacker appended the string `i18ntranslation` to the API URL path.

---

## Phase 2: Exploit Analysis

- **Credential Volume**: A total of **57, but 56 to be considered** unique combinations of usernames and passwords were used during the [Credential Stuffing](https://www.google.com/search?q=https://www.f5.com/glossary/credential-stuffing) attack.
	- To get list of all user credentials attempted.
```
 tshark -Y '(http.request.uri == "/bonita/loginservice") && (http.user_agent == "python-requests/2.28.1")' -r meerkat.pcap -T json | jq -r '.[]._source.layers["urlencoded-form"] | map(.) | "username=\"\(.[] | select(.["urlencoded-form.key"] == "username") | .["urlencoded-form.value"])\"&password=\"\(.[] | select(.["urlencoded-form.key"] == "password") | .["urlencoded-form.value"])\""'
```

- **Successful Compromise**: The successful login was achieved using the credentials `seb.broom@forela.co.uk:g0vernm3nt`.
    

---

## Phase 3: Persistence and Exfiltration

- **External Infrastructure**: The attacker utilized the text-sharing site **pastes.io** during the exploit.
- **Malicious Payload**: A public key file named **hffgra4unv** was used to gain persistence on the host.
- **System Modification**: The attacker modified the **/home/ubuntu/.ssh/authorized_keys** file to maintain access.
- **MITRE ATT&CK Mapping**: This persistence mechanism is categorized under MITRE technique ID **T1098.004** ([SSH Authorized Keys](https://attack.mitre.org/techniques/T1098/004/)).
