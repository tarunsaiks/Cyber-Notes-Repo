1. Discover probes using ICMP/Ping/Nmap on engagement scope (IP Addresses range) or Host Discovery
2. Service Discovery
3. Vulnerability Discovery

## Types of Testing

+ White Box
+ Black Box
+ Grey Box
Keep a strong eye on **SOW** (Statement of Work)

Find more about ![[Nmap#What is NMAP ?]]

## What is the Internet Control Message Protocol (ICMP)?

The Internet Control Message Protocol (ICMP) is a [network layer](https://www.cloudflare.com/learning/network-layer/what-is-the-network-layer/) protocol used by network devices to diagnose network communication issues. ICMP is mainly used to determine whether or not data is reaching its intended destination in a timely manner. Commonly, the ICMP [protocol](https://www.cloudflare.com/learning/network-layer/what-is-a-protocol/) is used on network devices, such as [routers](https://www.cloudflare.com/learning/network-layer/what-is-a-router/). ICMP is crucial for error reporting and testing, but it can also be used in [distributed denial-of-service (DDoS) attacks](https://www.cloudflare.com/learning/ddos/what-is-a-ddos-attack/)

## IP Subnetting

[CheatSheet](https://www.freecodecamp.org/news/subnet-cheat-sheet-24-subnet-mask-30-26-27-29-and-other-ip-address-cidr-network-references/)
+ ICMP Scanning all the IP Addresses in a range is called **Ping Sweep**.

# Ping :
#ping #linux_commands #network_commands
In Linux:
man page for ping [[ping]]

## Description

**ping** uses the ICMP protocol's mandatory ECHO_REQUEST datagram to elicit an ICMP ECHO_RESPONSE from a host or gateway. ECHO_REQUEST datagrams (''pings'') have an IP and ICMP header, followed by a struct timeval and then an arbitrary number of ''pad'' bytes used to fill out the packet.

Examples : 
```
ping 103.208.149.1 -c 1 // -c is used to count
```

+ To ping scan multiple IP's we use
```bash
for octet in {1..255}; do ping -c 1 103.208.149.$octet -W 1 >> ping_result.txt & done
```

> octet is variable name in bash script above and -W flag is used to timeout

+ To check the hosts that are alive, we use a simple bash script to format the IP's from above `ping_results.txt`
```bash
cat ping_results.txt | grep "bytes from" | cut -d " " -f4 | cut -d ":" -f1 > targets.txt
```

## Limitations of ping

+ Requires alot of file manipulation and bash scripting if working in real time scenarios
+ For NMAP, we can paste the IP's with ranges in a file and give it as input to work with ease.

# NMAP: 

```bash
nmap -iL ranges.txt -oA pingnmap.txt -PE
```

-iL : Input & List
-PE : Ping & ICMP Scan

Check for Cheatsheet below
![[nmap-cheatsheet-see_security_technologies.pdf]]

+ --min-hostgroup is used to scan multiple hosts in parallel. It does this by dividing the target IP space into groups and then scanning each group at a time.
+ default group size is five and max is 1024 (which creates a lot of network traffic)
+ [Official Book](https://nmap.org/book/man-performance.html)

