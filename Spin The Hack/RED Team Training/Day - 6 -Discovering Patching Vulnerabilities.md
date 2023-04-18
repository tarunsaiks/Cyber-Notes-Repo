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
#discovery #identify #vulnerability_discovery

Always follow Least Resistance Path (Firewall, Logs ..)

First we try to discover patching vulnerabilities on low hanging fruits (The services and versions running on ports after scanning)


## [CrackMapExec](https://wiki.porchetta.industries/)
Using crackmapexec, we can map the targets based on protocol and we can create a protocol specific list. 

Every protocol supports targets by CIDR notation(s), IP address(s), IP range(s), hostname(s), a file containing a list of targets or combination of all of the latter:CIDR notation(s), IP address(s), IP range(s), hostname(s), a file containing a list of targets or combination of all of the latter:

```bash
crackmapexec <protocol> <IP_ADDR>
crackmapexec <protocol> ms.evilcorp.org
crackmapexec <protocol> 192.168.1.0 192.168.0.2
crackmapexec <protocol> 192.168.1.0/24
crackmapexec <protocol> 192.168.1.0-28 10.0.0.1-67
crackmapexec <protocol> ~/targets.txt
```

### [Using Credentials](#using-credentials)

Every protocol supports using credentials in one form or another. For details on using credentials with a specific protocol, see the appropriate wiki section.

Generally speaking, to use credentials, you can run the following commands:

```bash
crackmapexec <protocol> <target(s)> -u username -p password
crackmapexec <protocol> <target(s)> -u username -p 'Admin!123@'
```


# Metasploit
#metasploit 

```bash
msfconsole
```

```bash
msf6 > search ssh
```

> Auxilary - We have to find if there is a vulnerbaility or not, **An auxiliary module does not execute a payload**.
> Exploit - Once we find there is vulnerability we use exploit.

# Process Flow

1. Host Discovery to get targets.txt
2. Lets say we have an IP Address of target, we directly jump into sub-phase B without host discovery, we directly start with Nmap, Open Ports, Versions.
3. crackmapexec to create protocol specific list or check for supported protocols
4. MSF --> protocol --> Auxilary --> Discover Patching Vulnerability.