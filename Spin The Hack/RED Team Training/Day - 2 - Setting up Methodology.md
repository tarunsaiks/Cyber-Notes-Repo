
+ A company always tries to reduce its cost by solving minimum work task and providing two things before a pentest 
	+ In-Scope and 
	+ Out-Scope

## Questions to ask before setting up methodology

1. Is there upto date track of IP Address and DNS?
2. Is there a routine patching (update) program? and its frequency.
	3. (Say Log4J v1 is being used and there is new patch due to log4j zero-day to v2.)
3. Do you use any commercial vulnerability scanner? (Nessus, Accunetix, Netsparker, Burp) And How often do you use it?
4. How do you manage old/ex-employee or admin details?
5. Do you use MFA (Multi Factor Authentication) in organization for particulars in scope?

## Red Teamer

+ Mindset of Hacker
+ Motive of a police
+ Performs Adversial Simulation.

#RedTeam #StepsInPenetrationTesting #Step1
# Information Gathering

## 1. Discover Network Hosts :

Things to do in Host Discovery
1. Find out IP Address of host
2. Find out DNS of host and in network.
3. Find out OS of host.
#nmap

Store the results of above things in a file `target.txt` and enquire with result with company to get in-scope domains and put the out-of-scope things in `ignore.txt`


## 2. Enumerate Listening Services :

Here we discover services which are listening and their respective port numbers.
Look out for these things in services and create a `ProtocolList.txt`
+ Service protocol (HTTPS, FTP, RDP, TCP, UDP, SMB)
+ Software Name and version.
#metasploit #wireshark #impacket
## 3. Discover Vulnerability

Check for below things and store results in `AttackVectors.txt`
+ Missing and Weak Credentials
+ Missing Security patches
+ Insecure configurations.
The `AttackVectors` file has list of all available attack vectors.

#RedTeam #StepsInPenetrationTesting #Step2
# Focused Pentesting

Now we have Authentication and security weakness information. Using this we deploy a backdoor, compromise vulnerable servers/services and Access RDP/SSH, Exploit missing software patches which leads to **building an INITIAL FOOTHOLD** 

#RedTeam #StepsInPenetrationTesting #Step3
# Post Exploitation & Privilege Escalation

Things to do in this phase are
+ Maintain Reliable Re-Entry (by establishing persistent meterpreter shell), 
+ Harvest Credentials (look for cleartext and hashed credentials)
+ Move Laterally (To escalate privileges horizontally)

Here we will perform Windows and Linux Privilege Escalation, Post Exploitation

#RedTeam #StepsInPenetrationTesting #Step4
# Documentation
+ Gather Evidence and Screenshots
+ Create Linear Narrative
+ Create final deliverable