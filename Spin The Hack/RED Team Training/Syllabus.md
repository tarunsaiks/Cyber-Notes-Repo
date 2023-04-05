+ Network Penetration Testing
	+ Data Breaches of Industries
		+ How hackers break-in?
	+ Adversial Attack Simulations
		+ INPT Workflow
	+ Needless Penetration Tester
		+ Low Hanging Fruit
		+ When a Pentest is Needless
	+ Phases of Internal Network Pentest
		+ Information Gathering
		+ Focused Penetration
		+ Post Exploitation & Previledge Escalation
		+ Documentation
	+ Setting up your Lab Environment
+ Phase 1 - ***Information Gathering***
	+ Discovering Network Hosts
		+ Engagement with Scope
		+ Internet Control Message Protocol (ICMP)
		+ Discovery with Nmap
		+ Other Host discovery methods
	+ Discovering Network Services
		+ Attacker Perspective of Network
		+ Port-Scanning with Nmap
		+ Parsing XML Output with Rub
	+ Discovering Network Vulnerabilities
		+ Understanding Vulnerability Discovery
		+ Discovering Patching Vulnerabilites
		+ Discoering Authentication Vulnerabilities
		+ Discovering Configuration Vulnerabilities
+ Phase 2 - ***Focused Penetration Testing***
	+ Attacking Vulnerable Web Services
		+ Understanding Phase 2
		+ Gaining an initial Foothold
		+ Compromising a vulnerable tomcat server
		+ Interactive Vs Non interactive shells
		+ Upgrading to an interactive shell
		+ Compromising a vulnerable jenkins server
	+ Attacking Database Services
		+ Compromising Microsoft SQL Server
		+ Stealing Windows Account Password Hashes
		+ Extracting Password Hashes with `CredDump`
	+ Attacking unpatched Services
		+ Understanding Software Exploits
		+ Understanding Typical Exploit Life Cycle
		+ Compromising MS17-010 with Metasploit
		+ The Meterpreter Shell payload
		+ Cautions about the public exploit database
+ Phase 3 - ***Post Exploitation & Privilege Escalation***
	+ Windows Post Exploitation
		+ Fundamentals of Post-Exploitation Objectives
		+ Maintaining reliable re-entry with meterpreter
		+ Harvesting Credentials with Mimikatz
		+ Harvesting Domain Cached Credentials
		+ Mocing Laterally with Pass-The-Hash
	+ Linux/UNIX Post-Exploitation
		+ Maintaining reliable re-entry with cron jobs
		+ Harvesting Credentials
		+ Escalating Privileges with SUID binaries
		+ Passing around SSH Keys
	+ Controlling the entire network
		+ Identifying Domain admin user accounts
		+ Obtaining domain admin privileges
		+ ntds.dit and the keys to kingdom