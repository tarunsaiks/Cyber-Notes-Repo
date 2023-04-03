
### What is Scanning ?

Set of procedures for identifying hosts, ports, and services, discovering the operating system of the target system, and identifying vulnerabilities and threats in the network. These scans are typically automated and give an insight into what could be exploited. Scanning reveals parts of the attack surface for attackers and allows launching targeted attacks to exploit the system.

### Scanning Types

+ **Passive Scanning** : Scanning a network without directly interacting with target machine. Passive scanning is usually carried out through packet capture and analysis tools like Wireshark; however, this technique only provides basic asset information like OS version, network protocol etc., against the target.
+ **Active Scanning** : Active scanning is a scanning method whereby you scan individual endpoints in an IT network to retrieve more detailed information. The active scan involves sending packets or queries directly to specific assets rather than passively collecting that data by "catching" it in transit on the network's traffic.

### **Network Scanning**

A network is usually a collection of interconnected hosts or computers to share information and resources. Network scanning helps to discover and map a complete network, including any live computer or hosts, open ports, IP addresses, and services running on any live host and operating system. Once the network is mapped, an attacker executes exploits as per the target system and services discovered. For example, a computer in a network with an outdated Apache version enables an attacker to launch an exploit against a vulnerable Apache server.

  

### **Port Scanning**

Per Wikipedia, "_In computer networking, a port is a number assigned to uniquely identify a connection endpoint and to direct data to a specific service. At the software level, within an operating system, a port is a logical construct that identifies a specific process or a type of network service_".

  

Port scanning is a conventional method to examine open ports in a network capable of receiving and sending data. First, an attacker maps a complete network with installed devices/ hosts like firewalls, routers, servers etc., then scans open ports on each live host. Port number varies between 0 to 65,536 based on the type of service running on the host. Port scanning results fall into the following three categories:

-   **Closed Ports**: The host is not listening to the specific port.
-   **Open Ports**: The host actively accepts a connection on the specific port.
-   **Filtered Ports**: This indicates that the port is open; however, the host is not accepting connections or accepting connections as per certain criteria like specific source IP address.

### **Vulnerability Scanning**

The vulnerability scanning proactively identifies the network's vulnerabilities in an automated way that helps determine whether the system may be threatened or exploited. Free and paid tools are available that help to identify loopholes in a target system through a pre-build database of vulnerabilities. Pentesters widely use tools such as [Nessus](https://www.tenable.com/products/nessus) and [Acunetix](https://www.acunetix.com/) to identify loopholes in a system.


## Nmap:

Nmap is a popular tool used to carry out port scanning, network discovery, identifying running services.

+ TCP SYN Scan (-sS) : Get the list of live hosts and associated ports on the hosts without completing the TCP three-way handshake and making the scan a little stealthier. 
	+ Usage: `nmap -sS MACHINE_IP`.
+ UDP Scan (-sU) : Gets the list of live hosts and associated ports on the hosts without completing the UDP. UDP scan works by sending a UDP packet to every targeted port. For most ports, this packet will be empty (no payload), but for a few of the more common ports a protocol-specific payload will be sent.
	+ Usage : `nmap -sU MACHINE_IP`.
-   **Ping Scan**: Allows scanning the live hosts in the network without going deeper and checking for ports services etc. 
	- Usage:  `nmap -sn MACHINE_IP`.
-   **Operating System Scan**: Allows scanning of the type of OS running on a live host. 
	- Usage: `nmap -O MACHINE_IP`.
-   **Detecting Services**: Get a list of running services on a live host. 
	- Usage: `nmap -sV MACHINE_IP`

Read more about Nmap switches here ![[Nmap#Nmap Switches]]


### **Nikto** -- [Read Blog](https://www.freecodecamp.org/news/an-introduction-to-web-server-scanning-with-nikto/)

Nikto is open-source software that allows scanning websites for vulnerabilities. It enables looking for subdomains, outdated servers, debug messages etc., on a website. You can access it on the AttackBox by typing `nikto -host MACHINE_IP`.


![[Nikto]]