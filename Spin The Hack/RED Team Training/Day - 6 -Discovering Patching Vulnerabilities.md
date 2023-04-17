After port scanning, we know which ports are open and which are closed. After this we need to know about any vulnerabilities in existing open ports and services running behind them.

Now we have, targets.txt, Open ports info, services running info, service version numbers. To attack any device (not that we will be hacking, but thinking in that mindset) we need to exploit these services if they are vulnerable, so let's check for vulnerabilities and try to patch them up to date.

`CVE - Common Vulnerability & Exposures`

# Vulnerability Discovery

Few ways to exploit vulnerabilities would be like
- Common credentials
- Version Numbers
- Web based Attacks

After parsing the XML output of nmap scan with NSE included, lets say we create a **Protocol Specific List** which contains
+ HTTPS - 192.168.0.1