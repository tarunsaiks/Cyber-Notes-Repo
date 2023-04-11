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
|53 | | 
