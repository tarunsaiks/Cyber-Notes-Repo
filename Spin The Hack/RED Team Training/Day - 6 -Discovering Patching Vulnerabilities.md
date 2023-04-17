After port scanning, we know which ports are open and which are closed. After this we need to know about any vulnerabilities in existing open ports and services running behind them.

Now we have, targets.txt, Open ports info, services running info, service version numbers. To attack any device (not that we will be hacking, but thinking in that mindset) we need to exploit these services if they are vulnerable, so let's check for vulnerabilities and try to patch them up to date.

`CVE - Common Vulnerability & Exposures`

# Vulnerability Discovery

Few ways to exploit vulnerabilities would be like
- Common credentials
- Version Numbers
- Web based Attacks

There will be vulnerabilies based on Authentication, Patching and Configuration using above things we'll try to find vulns.

After parsing the XML output of nmap scan with NSE included, lets say we create a **Protocol Specific List** which contains
+ HTTPS - 192.168.0.2:443; 192.168.1.2:443
+ SSH - 192.168.0.2:22; ...

## Tools
+ CrackMapExec
+ Medusa
+ Metasploit
+ Exploit-DB (service)
+ Webshot

> Using CrackMapExec, Medusa and Metasploit we can use common credentials 

> Using Metasploit and Exploit-DB we can identify patches

> Webshot gives analysis of web based attacks

# Discovering Patching Vulnerabilities

Always follow Least Resistance Path (Firewall, Logs ..)

First we try to discover patching vulnerabilities on low hanging fruits (The services and versions running on ports after scanning)


## CrackMapExec

