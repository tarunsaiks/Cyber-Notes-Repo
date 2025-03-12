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
## Protocols

`Protocols` are standardized rules that determine the formatting and processing of data to facilitate communication between devices in a network. These protocols operate at different layers within network models, each tailored to handle specific types of data and communication needs. Here’s a look at some common network protocols and their roles in data exchange.

#### Common Network Protocols

Network protocols are essential for defining how data is exchanged across networks. Each protocol operates at a specific layer of the OSI model, ensuring structured and efficient data handling.

|**Protocol**|**Description**|
|---|---|
|`HTTP (Hypertext Transfer Protocol)`|Primarily used for transferring web pages. It operates at the Application Layer, allowing browsers and servers to communicate in the delivery of web content.|
|`FTP (File Transfer Protocol)`|Facilitates the transfer of files between systems, also functioning at the Application Layer. It provides a way for users to upload or download files to and from servers.|
|`SMTP (Simple Mail Transfer Protocol)`|Handles the transmission of email. Operating at the Application Layer, it is responsible for sending messages from one server to another, ensuring they reach their intended recipients.|
|`TCP (Transmission Control Protocol)`|Ensures reliable data transmission through error checking and recovery, operating at the Transport Layer. It establishes a connection between sender and receiver to guarantee the delivery of data in the correct order.|
|`UDP (User Datagram Protocol)`|Allows for fast, connectionless communication, which operates without error recovery. This makes it ideal for applications that require speed over reliability, such as streaming services. UDP operates at the Transport Layer.|
|`IP (Internet Protocol)`|Crucial for routing packets across network boundaries, functioning at the Internet Layer. It handles the addressing and routing of packets to ensure they travel from the source to the destination across diverse networks.|

---

## Transmission

`Transmission` in networking refers to the process of sending data signals over a medium from one device to another. To further understand this concept, let’s examine the different types of transmission, the modes in which these transmissions can occur, and the media that carry the signals.

#### Transmission Types

`analog` and `digital`. 
Analog transmission uses continuous signals to represent information, commonly seen in traditional radio broadcasts.

Digital transmission employs discrete signals (bits) to encode data, which is typical in modern communication technologies like computer networks and digital telephony.

#### Transmission Modes

Transmission modes define how data is sent between two devices. 

`Simplex` mode allows one-way communication only.
`Half-duplex` mode permits two-way communication but not simultaneously;
`Full-duplex` mode, used in telephone calls, supports two-way communication simultaneously.

#### Transmission Media

Can be wired or wireless. 

Wired media includes `twisted pair` cables, commonly used in Ethernet networks and local area network (LAN) connections; `coaxial` cables, used for cable TV and early Ethernet; and `fiber optic` cables, which transmit data as light pulses and are essential for high-speed internet backbones. Wireless media, on the other hand, encompasses `radio waves` for Wi-Fi and cellular networks, `microwaves` for satellite communications, and `infrared` technology used for short-range communications like remote controls. Each type of media has its specific use cases depending on the requirements of the network environment.

# Components of Network

| **Component**                           | **Description**                                           |
| --------------------------------------- | --------------------------------------------------------- |
| `End Devices`                           | Computers, Smartphones, Tablets, IoT / Smart Devices      |
| `Intermediary Devices`                  | Switches, Routers, Modems, Access Points                  |
| `Network Media and Software Components` | Cables, Protocols, Management and Firewalls Software      |
| `Servers`                               | Web Servers, File Servers, Mail Servers, Database Servers |

## End Devices

- Hosts
- PC, Smartphones, refrigerator, smart TV's
-  users routinely interact with them directly to perform tasks like browsing the web, sending messages, and creating documents.
- serve as the primary user interface to the world wide web, enabling users to access network resources and services seamlessly
## Intermediary Devices

- Facilitates flow of data between end devices
- routers, switches, modems, and access points
- responsible for `packet forwarding`, connect networks and control traffic to enhance performance and reliability, they ensure smooth transmission and prevent congestion.
- `firewalls` protect certain networks from unauthorized access and potential threats.
#### Network Interface Cards (NICs)

- A `Network Interface Card (NIC)` is a hardware component installed in a computer, or other device, that enables connection to a network. 
- It provides the physical interface between the device and the network media, handling the sending and receiving of data over the network. 
- Each NIC has a **unique Media Access Control (MAC) address**, which is essential for devices to identify each other, and facilitate communication at the data link layer. 
- NICs can be designed for wired connections, such as Ethernet cards that connect via cables, or for wireless connections, like Wi-Fi adapters utilizing radio waves. 
- For example, a desktop computer might use a wired NIC, along with an Ethernet cable, to connect to a local network, while a laptop uses a wireless NIC to connect via Wi-Fi.

#### Routers

A `router` is an intermediary device that plays a hugely important role - the forwarding of data packets between networks, and ultimately directing internet traffic. Operating at the network layer (Layer 3) of the OSI model, routers read the network address information in data packets to determine their destinations. They use routing tables and routing protocols—such as `Open Shortest Path First (OSPF)` or `Border Gateway Protocol (BGP)`—to find the most efficient path for data to travel across interconnected networks, including the internet.

They fulfill this role by `examining incoming data packets` and forwarding them toward their destinations, based on IP addresses. By `connecting multiple networks`, routers enable devices on different networks to communicate. They also manage network traffic by selecting optimal paths for data transmission, which helps prevent congestion—a process known as `traffic management`. Additionally, routers enhance `security` by incorporating features like firewalls and access control lists, protecting the network from unauthorized access and potential threats.

#### Switches

The `switch` is another integral component, with it's primary job being to connect multiple devices within the same network, typically a Local Area Network (LAN). Operating at the data link layer (Layer 2) of the OSI model, switches use MAC addresses to forward data only to the intended recipient. By managing data traffic between connected devices, switches reduce network congestion and improve overall performance. They enable devices like computers, printers, and servers to communicate directly with each other within the network. For instance, in a corporate office, switches connect employees' computers, allowing for quick file sharing and access to shared resources like printers and servers.

#### Hubs

A `hub` is a basic (and now antiquated) networking device. It connects multiple devices in a network segment and broadcasts incoming data to all connected ports, regardless of the destination. Operating at the physical layer (Layer 1) of the OSI model, hubs are simpler than switches and do not manage traffic intelligently. This indiscriminate data broadcasting can lead to network inefficiencies and collisions, making hubs less suitable for modern networks. For example, in a small home network setup from earlier times, a hub might connect a few computers, but today, switches are preferred due to their better performance and efficiency.