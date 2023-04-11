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

When port scanning we need not understand how the services are running and how to work with services, we just focus on status of the port.

## Active or Passive ?

The port scanning can be both passive as well as active based on service detection and aggresion of the scan type, it depends on the scan type. Lets say if we are scanning with `-A` and creating alot of traffic in network then it is active.

## Normal Scanning

```bash
$ nmap -Pn -p 21,22, 
```
