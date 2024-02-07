```mermaid
flowchart TD
	id1([Use Nmap for Port Scanning and NSE Scans]) --> id2[targets.txt]
	id2[targets.txt] --> id3[Nmap Port Scan]
	%%id3 -->|Enumerate Services listening on open ports to learn more|%% 
	id2 --> id4[NSE Scripts]
	id3 --> id5{{Open Ports}}
	id3 --> id6{{Service Protocols}}
	id3 --> id7{{Software Info}}
	id5 <-.-> id6
	id6 <-.-> id7
	id4 --> id9{{Configuration Details}}
	%%id7 <-.-> id9%%
	id5 & id6 & id7 & id9 --> id10{{Parse XML Output}}
```

## Port Scanning ?

Regardless of what services are running behind a port, we just try to check if a particular port is opne or closed or filtered. There will be different services running behind different ports. For Example

| Port | Service Running |
|--|--|
|21 | FTP|
|22 | SSH |
|25 | SMTP |
|53| DNS|
|80 | HTTP |
|389 |LDAP |
|443 |HTTPS |
|445 | Microsoft SMB |
|1433 | Microsoft SQL Server|
|3306| MySQL Server|
|5800 | Java VNC Server |
|5900 | VNC Server |

>Virtual Network Computing, or VNC, is an open source application that **provides screen sharing services** and is available for virtually all operating systems such as Windows, Linux, and of course OS X.

When port scanning we need not understand how the services are running and how to work with services, we just focus on status of the port.

## Active or Passive ?

The port scanning can be both passive as well as active based on service detection and aggresion of the scan type, it depends on the scan type. Lets say if we are scanning with `-A` and creating alot of traffic in network then it is active.

## Normal Scanning

```bash
$ nmap -Pn -p 21,22,80,443,445,3306,5800-5900 -iL targets.txt -oA quickscan
```

Here we are scanning without host discovery of mentioned ports and IP's from input file `targets.txt` and saving the output in a file named `quickscan`

## Fingerprinting

Fingerprinting is a process in which we try to gather more information on ports like services running and their versions. For this it establishes a handshake with that port.

> w3challs.com is a testing website we are using here to scan and learn more about port scanning with nmap

Here we try to aggressively scan a particular host to gather as much information as we can using service detection and fingerprinting.

Here if we try scanning any corporate domain, we will create a lot of network traffic for which we are not authorized, Instead we'll scan a training website like `w3challs.com`

```bash
$ nslookup w3challs.com --> 51.15.18.162
$ nmap -Pn 51.15.18.162 -p- -sV -A -oA full --min-rate 50000 -vv
```

This takes quite some time to give all the results including service detection scan. To tackle this time problem, first we'll scan with partial connection like we did with `quick`  output.

Based on the open ports from that quick file, we add only those ports in the fingerprinting nmap scan command.


# NSE Scripts

The Nmap Scripting Engine (NSE) is one of Nmap's most powerful and flexible features. It allows users to write (and share) simple scripts (using the [Lua programming language](http://lua.org/) ) to automate a wide variety of networking tasks. Those scripts are executed in parallel with the speed and efficiency you expect from Nmap. Users can rely on the growing and diverse set of scripts distributed with Nmap, or write their own to meet custom needs.

Nmap Scripting Engine default scripts will be stored in /usr/share/local/nmap/scripts

## Types of Nmap scripts

When we talk about writing NSE scripts, there are four different types that can help us enhance the default Nmap features, depending on the target and the scanning phase in which they are run.

1.  **Prerule scripts:** These types of scripts run before the rest of any scanning operation, while Nmap doesn't have any data about the remote target.
2.  **Host scripts:** Once the Nmap default scan has finished the host exploration, detection, port scanning or software discovery, it will perform the host scripts.
3.  **Service scripts:** These are a particular set of Nmap scripts that are run against services on the remote host. These include http service scripts, for example, which can be run against web servers.
4.  **Postrule scripts:** These are run after the entire Nmap scan has finished, and are often useful for parsing, formatting and presenting the different results.

<table>
<thead>
<tr>
<th>Nmap Script Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>auth</td>
<td>All sorts of authentication and user privilege scripts</td>
</tr>
<tr>
<td>broadcast</td>
<td>Network discovery scripts that use broadcast petitions for intel gathering</td>
</tr>
<tr>
<td>brute</td>
<td>Set of scripts for performing brute force attacks to guess access credentials</td>
</tr>
<tr>
<td>default</td>
<td>The most popular Nmap scripts, using -sC by default</td>
</tr>
<tr>
<td>discovery</td>
<td>Scripts related to network, service and host discovery</td>
</tr>
<tr>
<td>dos</td>
<td>Denial of service attack scripts used to test and perform DOS and floods</td>
</tr>
<tr>
<td>exploit</td>
<td>Used to perform service exploitation on different CVEs</td>
</tr>
<tr>
<td>external</td>
<td>Scripts that rely on 3rd party services or data</td>
</tr>
<tr>
<td>fuzzer</td>
<td>Used to perform fussing attacks against apps, services or networks</td>
</tr>
<tr>
<td>intrusive</td>
<td>All the ‘aggressive’ scripts that cause a lot of network noise</td>
</tr>
<tr>
<td>malware</td>
<td>Malware detections and exploration scripts</td>
</tr>
<tr>
<td>safe</td>
<td>Safe and non-intrusive/noisy scripts</td>
</tr>
<tr>
<td>version</td>
<td>OS, service and software detection scripts</td>
</tr>
<tr>
<td>vuln</td>
<td>The <a href="/blog/nmap-vulnerability-scan" title="How to Perform a Nmap Vulnerability Scan using NSE scripts">Nmap vuln</a> category includes vulnerability detection and exploitation scripts</td>
</tr>
</tbody>
</table>

## XML File Parsing

Use this scipt to convert XML to CSV [Github](https://github.com/laconicwolf/Nmap-Scan-to-CSV)