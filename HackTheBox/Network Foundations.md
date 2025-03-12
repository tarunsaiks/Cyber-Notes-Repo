# Introduction to Networks
## What is Network

Collection of inter-connected devices

Nodes - individual devices
Links - Communication pathways that connect nodes (wired or wireless)
Data Sharing - main objective and purpose of network

## Why Networks are Important?

- Resource sharing
- Communication
- Data Access overcoming physical presence limitations
- Collaboration - people around the world can collaborate and work without physically being there.

## Types of Networks

### LAN

- Covers small area
- owned by single person or organization
- high data transfer
- uses wired or wireless connections
- in-expensive
![](../Pasted%20image%2020250312142027.png)
### WAN

- Covers Cities, countries or continents
- collectively owned or distributed ownership (ISP)
- slower data transfer speed due to long distance (Long-Distance always sucks T_T)
- uses fiber optics, underwater sea cables, satellites and leased telecommunication lines.
- costly and complex

![](../Pasted%20image%2020250312142200.png)

## LAN and WAN Work together, but How??

LAN in Asia can connect to WAN and LAN in America can also connect to WAN. establishing connections, INTERNET.

A home LAN connects to an Internet Service Provider's (ISP) WAN, granting internet access to all devices within the home network. A modem bridges the connection, converting digital signals into suitable formats for transmission over various media. In business settings, WANs enable unified communication and collaboration across different locations, enhancing productivity. At home, devices connect to a router, managing local traffic and communicating with the ISP's WAN, allowing access to global content and services beyond the local network.

<div style="page-break-after: always;"></div>

# Network Concepts

Everything we see that is Internet today, is built on top of **TCP/IP** stack. #TCP/IP
## OSI Model

But OSI model is a conceptual framework that standardizes the functions of a network into seven layers. 
1. Physical - raw bit streams over physical medium; Ethernet cables, hubs and repeaters.
2. Data Link - node-to-node transfer; data frames transmitted over proper synchronization and error detection and correction; Switches and bridges operate using MAC (Media Access Control) addresses to identify network devices; MAC Table
3. Network - Packets; Packet forwarding and path determination, using routing tables; IP addresses to identify devices and determine most efficient path and transmission.
4. Transport - end-to-end communication services for applications, responsible for reliability of data transfer (TCP - connection-oriented, error recovery, if not UDP - connectionless without any guarantee of delivery)
5. Session - establishes, manages and terminates connections; manages sessions between applications;  session checkpointing and recovery; Protocols and `APIs (Application Programming Interfaces)` operating at this layer coordinate communication between systems and applications.
6. Presentation -  translator between the application layer and the network format; data encryption and decryption, data compression, and converting data formats.
7. Application - Common protocols - HTTP, FTP, DNS, SMTP

## TCP/IP Model

Condensed OSI model with 5 layers - Link Layer, Internet Layer, Transport Layer, Application Layer.
![TCP/IP Stack](https://academy.hackthebox.com/storage/modules/289/network_concepts/TCP_IP.png)