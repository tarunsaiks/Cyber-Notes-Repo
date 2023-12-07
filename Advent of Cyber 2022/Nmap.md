
## What is NMAP ?

Nmap is a network scanner created by Gordon Lyon. Nmap is used to discover hosts and services on a computer network by sending packets and analyzing the responses. Nmap provides a number of features for probing computer networks, including host discovery and service and operating system detection


## Nmap Switches
The switches questions in Nmap Introduction are way more difficult and I tried searching in man page, but wasn't of much use without carefully reading and understanding it. So next time you think of nmap, give it's man page an entire look from top to bottom, it deserves it and you're screwed if you neglect understanding it. 

[https://grumpyghost1011.medium.com/nmap-room-tryhackme-walkthrough-%EF%B8%8F-4fdf25829f1d](https://grumpyghost1011.medium.com/nmap-room-tryhackme-walkthrough-%EF%B8%8F-4fdf25829f1d)  Here is a link to walkthrough posted by someone in Medium, it's helpful

+  What is the first switch listed in the help menu for a 'Syn Scan' (more on this later!)? 
	+ `-sS` 
+ Which switch would you use for a "UDP scan"? 
	+ `-sU `
+ If you wanted to detect which operating system the target is running on, which switch would you use? 
	+ `-O `
+ Nmap provides a switch to detect the version of the services running on the target. What is this switch? 
	+ `-sV `

+ The default output provided by nmap often does not provide enough information for a pentester. How would you increase the verbosity? 
	+ `-v `

+ Verbosity level one is good, but verbosity level two is better! How would you set the verbosity level to two? (Note: it's highly advisable to always use at least this option) 
	+  `-vv `

+ We should always save the output of our scans -- this means that we only need to run the scan once (reducing network traffic and thus chance of detection), and gives us a reference to use when writing reports for clients. 

+ What switch would you use to save the nmap results in three major formats? 
	+ `-oA `

+ What switch would you use to save the nmap results in a "normal" format? 
	+ `-oN `

+ A very useful output format: how would you save results in a "grepable" format? 
	+ `-oG `

+ Sometimes the results we're getting just aren't enough. If we don't care about how loud we are, we can enable "aggressive" mode. This is a shorthand switch that activates service detection, operating system detection, a traceroute and common script scanning. 

+ How would you activate this setting? 

	+ `-A `

+ Nmap offers five levels of "timing" template. These are essentially used to increase the speed your scan runs at. Be careful though: higher speeds are noisier, and can incur errors! 

+ How would you set the timing template to level 5? 

	+ `-T5` 

We can also choose which port(s) to scan. 

+ How would you tell nmap to only scan port 80? 
	+ `-p 80 `

+ How would you tell nmap to scan ports 1000-1500? 
	+ `-p 1000-1500 `

+ How would you tell nmap to scan all ports? 
	+ `-p- `

+ How would you activate a script from the nmap scripting library (lots more on this later!)? 
	+ `--script `

+ How would you activate all of the scripts in the "vuln" category? 
	+ `--script=vuln`

## TCP Scan Types
To understand TCP Connect scans (-sT), it is important to understand how the TCP handshake occurs. 

THREE WAY HANDSHAKE: 
![[3way_handshake.png]]

The packets sent over the ethernet performing TCP Handshake are as shown below: 
![[3way_wireshark.png]]

-   A TCP Connect scan works by performing the three-way handshake with each target port in turn. In other words, Nmap tries to connect to each specified TCP port, and determines whether the service is open by the response it receives. 
-   if Nmap sends a TCP request with the SYN flag set to a closed port, the target server will respond with a TCP packet with the RST (Reset) flag set. By this response, Nmap can establish that the port is closed. 
    
-   ![[RST for closed ports.png]]

This is all well and good, however, there is a third possibility. What if the port is open, but hidden behind a firewall? 

**Many firewalls are configured to simply drop incoming packets. Nmap sends a TCP SYN request, and receives nothing back. This indicates that the port is being protected by a firewall and thus the port is considered to be filtered.** 

That said, it is very easy to configure a firewall to respond with a RST TCP packet. For example, in IPtables for Linux, a simple version of the command would be as follows:
![[iptables-cmd.png]]


## TCP SYN Scans
-   As with TCP scans, SYN scans (-sS) are used to scan the TCP port-range of a target or targets; however, the two scan types work slightly differently. SYN scans are sometimes referred to as "Half-open" scans, or "Stealth" scans. 

-   Where TCP scans perform a full three-way handshake with the target, SYN scans sends back a RST TCP packet after receiving a SYN/ACK from the server (this prevents the server from repeatedly trying to make the request). In other words, the sequence for scanning an open port looks like this: 

-   Advnatages for Hackers :  
    
    -   It can bypass older IDS as they look out for only 3 way handshakes which is not the case with Modern IDS 
        
    -   SYN Scans are often not logged by applications listening on ports, standard procedure is to log it only after successful handshake. SYN scans are usually faster than the TCP Connect scan 
        
    
-   Disadvantages:  
    -   They require sudo permission to work properly, coz SYN needs to create raw packets (as opposed to full handshake) which is privileged only to root user by default. 

-   For pros, over cons, SYN scans are used as default by Nmap if run with sudo permissions, else TCP Connect scan. 
-   If a port is closed, server responds with RST TCP packet, if port is filtered by the firewall, TCP SYN packet is either dropped, or spoofed with a TCP reset. 
-  SYN scans can also be made to work by giving Nmap the CAP_NET_RAW, CAP_NET_ADMIN and CAP_NET_BIND_SERVICE capabilities; however, this may not allow many of the NSE scripts to run properly.


## UDP Scans

+ Nmap switch for UDP scan is (-sU). 
+ Connections are stateless, unlike TCP, UDP scans do not expect to receive the ACK (makes it more difficult and consume more time). They just send packets to the target port and hope they make it. 
+ When a packet is sent to Open UDP port, there should be no response, Nmap refers it as open|filtered (port is either open or suspected to be firewalled). 
+ When a packet is sent to a closed UDP port, target usually responds back with an ICMP (ping) packet containing a message that port is unavailable, Nmap then marks it as Closed. 
+ Top ports of target can be scanned using the switch --top-ports <number>

## NULL, FIN and XMAS
-   NULL, FIN and Xmas are generally used for Firewall Evasion, it used to work with older IDS. When it receives a malformed packets, it usually responds with a RST packet if port is closed or won't respond at all for open packets. 
    
-   In practice, in particular Cisco Network devices and Microsoft Windows, they respond with RST packet to any malformed TCP packet regardless of port being open or closed.\


### NULL: 

-   (-sN) scans are when TCP request is sent with no flag set at all, then as per RFC, the host should respond with a RST if port is closed. 
- ![[NULL.png]]

### FIN: 

-   (-sF) works in almost same way, except request is sent with FIN flag set (usually used to gracefully close an active connection), RST if port is closed.
- ![[FIN.png]]

### Xmas: 

-   Xmas scans (-sX) send a malformed TCP packet and expects a RST response for closed ports. It's referred to as an xmas scan as the flags that it sets (PSH, URG and FIN) give it the appearance of a blinking christmas tree when viewed as a packet capture in Wireshark. 
-   ![[Xmas.png]]

If the port is open then there is no response to the malformed packet. Unfortunately (as with open UDP ports), that is also an expected behaviour if the port is protected by a firewall, so NULL, FIN and Xmas scans will only ever identify ports as being open|filtered, closed, or filtered. If a port is identified as filtered with one of these scans then it is usually because the target has responded with an ICMP unreachable packet.

### ICMP Networking

+ Nmap usually send a ping sweep (-sn) to a group of IP addresses, can be done using range (192.168.12.25-255) or CIDR notation (192.168.12.25/24).

### NSE (Nmap Scripting Engine)

-   It is developed using language Lua. 
-   They do variety of things from scanning vulnerablities to automating exploits for them. It is particularly useful for reconnaisance. 
-   Categories include safe, intrusive, vuln, exploit, auth, brute and discovery