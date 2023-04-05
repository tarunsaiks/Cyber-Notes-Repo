+ INPT - Internal Network Penetration Testing

## Introduction

+ We have many organization and which have faced alot of cyber attacks - Specifically Data breaches. Few of the examples are 
	+ Log4J
	+ Solarwinds
	+ Twitch Code and Data Base Leak
+ These data breaches are performed by black hat hackers with different intents

## How Hackers break-in?

+ In every organization the data breach conists of two parties, Attacker and Defender.
+ In a typical corporate network infrastructure, there exists alot of points from where attacker can break-in a network/application. This is called **ATTACK SURFACE**

> An attack surface is **the entire area of an organization or system that is susceptible to hacking**. It's made up of all the points of access that an unauthorized person could use to enter the system.

+ The Defender is usually given a task to secure these point of entry by performing monitor network traffic, respond to alerts from any devices or unwanted traffic, which is usually Overwhelming.

## Adverse Attack Simulation
-  Adverse - preventing success or development; harmful; unfavourable.
- Attack Simulation - Simulating a attack in a closed environment

### How to perform Adverse Attack Simulation
+ we use INPT to perform the attack simulation

### INPT Workflow :
#StepsInPenetrationTesting
Steps in INPT
 
1. Information Gathering
	1.  Discovering Network Hosts (IP Address Range - Identify a host with its IP address which will be attacked)
	2. Enumerate listening services (Check for Protocols, Open ports, services with vulnerabilities)
	3. Discover Vulnerable Attack Surface
2. Focused Penetration Testing
	1. Compromising/Attacking Vulnerable Host
		1. Exploit Missing Software patches (Ex ; Log4J)
		2. Deploy custom executable payloads 
		3. Access remote management interface (Persistence, to automatically extract data)
3. Post Exploitation and Privilege escalation
	1. Establish reliable re-entry
	2. Harvesting Credentials
	3. Move laterallly and Escalation
4. Documentation
	1. Gathering Evidence / Screenshots
	2. Create linear attack narratives (Explain the approach from start to end with details)
	3. Create final deliverable PoC report.