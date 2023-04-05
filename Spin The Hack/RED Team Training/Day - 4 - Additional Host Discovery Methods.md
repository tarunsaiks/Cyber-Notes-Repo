## IP Subnetting cheatsheet

BGP Toolkit - bgp.he.net

In IP's, the host address ending with say 10.0.0.x/24 ---> There's always a host active with IP 10.0.0.1 which will be mostly assigned to Gateway/ Firewall.

Sometimes the company does not provide entire IP range, here we will have to manually search for subnets and groups to check for hosts. -- **This is additional Host discovery methods**
```bash
nmap -sn 103.0-255.0-255.1 -PE --min-hostgroup 10000 --min-rate 10000 > ranges.txt
```

After pinging all the IP's ending with `.1` and if we discover hosts, then we create a range to check for all the hosts in that subdomain.

## Steps in using Nmap
1. Generate targets.txt
2. perform a nmap port scan 
	1. Get info on open ports --> **enumerate services listening on open ports**
	2. service protocols
	3. software information
3. NSE scripts scan
	1. Configuration details

## Banner Grabbing
#whatweb #banner_grabbing
After differentiating between ports and services, we use a tool **`whatweb`** which is used to perform banner grabbing.
