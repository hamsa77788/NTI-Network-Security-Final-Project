# NTI Network Security Final Project

## 📌 Project Overview

This project was developed as the final project of the NTI Network Security training using Cisco Packet Tracer.

The project demonstrates the practical implementation of a complete multi-network infrastructure consisting of multiple LANs connected through three routers. The network was designed using VLSM subnetting according to the number of hosts required in each network.

The project also includes static routing, a centralized DHCP server, DHCP relay, DNS, a web server, switches, PCs, and wireless Access Points.

The main goal of the project was to apply the networking concepts covered throughout the training and build a functional network in which devices across different networks can communicate and access the required network services.

---

## 🎯 Project Objectives

The main objectives of this project were to:

- Design a multi-network topology using Cisco Packet Tracer.
- Divide the network into multiple subnets using VLSM.
- Determine the appropriate subnet size based on the required number of hosts.
- Calculate network addresses, usable IP ranges, and broadcast addresses.
- Configure routers and switches.
- Connect multiple LANs through three routers.
- Configure static routing between the routers.
- Implement a centralized DHCP server.
- Configure DHCP relay using `ip helper-address`.
- Configure a DNS server.
- Configure a web server.
- Host a custom website inside Cisco Packet Tracer.
- Provide wireless connectivity using Access Points.
- Verify communication between different networks.
- Provide access to network services from different subnets.

---

# 🏗️ Network Topology

The topology consists of **9 networks** connected through **3 routers**.

### Main Components

- **3 Routers**
- **6 Switches**
- **3 Servers**
- **2 Access Points**
- Multiple PCs and laptops
- **9 IP Networks**

The network is divided into six LANs and three point-to-point networks used to connect the routers.

### Router Distribution

- **Router 0**
  - Network 3
  - Network 4
  - Network 7
  - Network 8

- **Router 1**
  - Network 1
  - Network 2
  - Network 7
  - Network 9

- **Router 2**
  - Network 5
  - Network 6
  - Network 8
  - Network 9

---

# 🌐 IP Addressing and VLSM Subnetting

VLSM (Variable Length Subnet Masking) was used to allocate IP addresses efficiently according to the number of hosts required in each network.

Larger subnets were assigned to networks requiring more hosts, while smaller `/30` subnets were used for the point-to-point router connections.

The addressing scheme is based on the `192.168.1.0/24` address space.

---

## 🖧 Network 3

### Subnet Information

| Parameter | Value |
|---|---|
| Hosts Needed | 50 |
| Available Hosts | 62 |
| Unused Hosts | 12 |
| Network Address | `192.168.1.0` |
| CIDR | `/26` |
| Subnet Mask | `255.255.255.192` |
| Usable Range | `192.168.1.1 - 192.168.1.62` |
| Broadcast | `192.168.1.63` |

### Devices

Network 3 contains:

- 15 PCs
- 1 DHCP Server
- 1 Cisco Server / Web Server
- 1 Switch
- Router 0 interface

### Gateway

The default gateway for Network 3 is:

`192.168.1.1`

### Servers

Network 3 contains the centralized DHCP server and the web server used by the project.

---

## 🖧 Network 4

### Subnet Information

| Parameter | Value |
|---|---|
| Hosts Needed | 50 |
| Available Hosts | 62 |
| Unused Hosts | 12 |
| Network Address | `192.168.1.64` |
| CIDR | `/26` |
| Subnet Mask | `255.255.255.192` |
| Usable Range | `192.168.1.65 - 192.168.1.126` |
| Broadcast | `192.168.1.127` |

### Devices

Network 4 contains:

- 18 PCs
- 2 Laptops
- 1 Switch
- 1 Access Point
- Router 0 interface

### Gateway

The default gateway for Network 4 is:

`192.168.1.65`

### Wireless Connectivity

An Access Point is connected to Network 4 to provide wireless connectivity for the two laptops.

---

## 🖧 Network 1

### Subnet Information

| Parameter | Value |
|---|---|
| Hosts Needed | 20 |
| Available Hosts | 30 |
| Unused Hosts | 10 |
| Network Address | `192.168.1.128` |
| CIDR | `/27` |
| Subnet Mask | `255.255.255.224` |
| Usable Range | `192.168.1.129 - 192.168.1.158` |
| Broadcast | `192.168.1.159` |

### Devices

Network 1 contains:

- 16 PCs
- 1 Switch
- Router 1 interface

### Gateway

The default gateway for Network 1 is:

`192.168.1.129`

---

## 🖧 Network 2

### Subnet Information

| Parameter | Value |
|---|---|
| Hosts Needed | 20 |
| Available Hosts | 30 |
| Unused Hosts | 10 |
| Network Address | `192.168.1.160` |
| CIDR | `/27` |
| Subnet Mask | `255.255.255.224` |
| Usable Range | `192.168.1.161 - 192.168.1.190` |
| Broadcast | `192.168.1.191` |

### Devices

Network 2 contains:

- 14 PCs
- 6 Laptops
- 1 Switch
- 1 Access Point
- Router 1 interface

### Gateway

The default gateway for Network 2 is:

`192.168.1.161`

### Wireless Connectivity

An Access Point is connected to Network 2 to provide wireless connectivity for the laptops.

---

## 🖧 Network 5

### Subnet Information

| Parameter | Value |
|---|---|
| Hosts Needed | 12 |
| Available Hosts | 14 |
| Unused Hosts | 2 |
| Network Address | `192.168.1.192` |
| CIDR | `/28` |
| Subnet Mask | `255.255.255.240` |
| Usable Range | `192.168.1.193 - 192.168.1.206` |
| Broadcast | `192.168.1.207` |

### Devices

Network 5 contains:

- 10 PCs
- 1 DNS Server
- 1 Switch
- Router 2 interface

### Gateway

The default gateway for Network 5 is:

`192.168.1.193`

### DNS Server

The DNS server is configured with:

`192.168.1.195`

---

## 🖧 Network 6

### Subnet Information

| Parameter | Value |
|---|---|
| Hosts Needed | 12 |
| Available Hosts | 14 |
| Unused Hosts | 2 |
| Network Address | `192.168.1.208` |
| CIDR | `/28` |
| Subnet Mask | `255.255.255.240` |
| Usable Range | `192.168.1.209 - 192.168.1.222` |
| Broadcast | `192.168.1.223` |

### Devices

Network 6 contains:

- 10 PCs
- 1 Switch
- Router 2 interface

### Gateway

The default gateway for Network 6 is:

`192.168.1.209`

---

# 🔗 Router-to-Router Networks

Networks 7, 8, and 9 are dedicated point-to-point networks used to connect the three routers.

A `/30` subnet was selected because a point-to-point connection requires only two usable IP addresses.

---

## Network 7 — Router 0 ↔ Router 1

| Parameter | Value |
|---|---|
| Network Address | `192.168.1.224` |
| CIDR | `/30` |
| Subnet Mask | `255.255.255.252` |
| Usable Range | `192.168.1.225 - 192.168.1.226` |
| Broadcast | `192.168.1.227` |

### Router Interfaces

- Router 0: `192.168.1.225`
- Router 1: `192.168.1.226`

---

## Network 8 — Router 0 ↔ Router 2

| Parameter | Value |
|---|---|
| Network Address | `192.168.1.228` |
| CIDR | `/30` |
| Subnet Mask | `255.255.255.252` |
| Usable Range | `192.168.1.229 - 192.168.1.230` |
| Broadcast | `192.168.1.231` |

### Router Interfaces

- Router 0: `192.168.1.229`
- Router 2: `192.168.1.230`

---

## Network 9 — Router 1 ↔ Router 2

| Parameter | Value |
|---|---|
| Network Address | `192.168.1.232` |
| CIDR | `/30` |
| Subnet Mask | `255.255.255.252` |
| Usable Range | `192.168.1.233 - 192.168.1.234` |
| Broadcast | `192.168.1.235` |

### Router Interfaces

- Router 1: `192.168.1.233`
- Router 2: `192.168.1.234`

---

# 🔀 Static Routing

Static routing was implemented to allow communication between the different networks connected through the three routers.

Each router was configured with routes to remote networks using:

- Destination network
- Subnet mask
- Next-hop IP address

### Router 0

Router 0 is directly connected to:

- Network 3
- Network 4
- Network 7
- Network 8

It uses static routes to reach the networks behind Router 1 and Router 2.

### Router 1

Router 1 is directly connected to:

- Network 1
- Network 2
- Network 7
- Network 9

It uses static routes to reach the networks behind Router 0 and Router 2.

### Router 2

Router 2 is directly connected to:

- Network 5
- Network 6
- Network 8
- Network 9

It uses static routes to reach the networks behind Router 0 and Router 1.

The three point-to-point networks provide the paths between the routers.

---

# 🌐 DHCP Configuration

A centralized DHCP server was configured in **Network 3**.

The DHCP server automatically provides network configuration to clients.

The DHCP service provides:

- IP Address
- Subnet Mask
- Default Gateway
- DNS Server information

Instead of configuring a separate DHCP server for every network, one centralized DHCP server is used.

---

## DHCP Relay

DHCP requests are broadcast messages, and routers do not normally forward broadcasts between different networks.

To allow clients in remote networks to communicate with the centralized DHCP server, DHCP relay was configured using:


ip helper-address
The appropriate router interfaces forward DHCP requests toward the DHCP server located in Network 3.

This allows clients in different subnets to obtain their IP configuration automatically from the centralized DHCP server.

---

# 🔎 DNS Configuration

A DNS server was configured in **Network 5**.

The DNS server is responsible for resolving domain names into IP addresses.

The DNS server is configured with the IP address:

`192.168.1.195`

Clients can use the DNS server to resolve the domain associated with the project web server instead of accessing the server directly using its IP address.

---

# 🖥️ Web Server

A Cisco Server was configured in **Network 3** to host the project website.

The server uses the IP address:

`192.168.1.10`

The web server provides access to a custom website created specifically for the project.

The website documents the network and presents information about the implemented services.

---

# 🌍 Project Website

A custom website was created and hosted inside Cisco Packet Tracer.

The website provides an interactive overview of the project and its network services.

### Website Sections

The website includes information about:

- Network topology
- Network services
- DHCP
- DNS
- Web Server
- Static Routing
- Network Overview
- Project Information

### Network Overview

The topology presented on the website consists of:

- **9 Networks**
- **3 Routers**
- **6 Switches**
- **3 Servers**
- **2 Access Points**

The website was accessed from a laptop using the Packet Tracer Web Browser.

---

# 📡 Wireless Networking

Two Access Points were implemented in the topology.

### Access Point 1

The first Access Point is connected to **Network 4** and provides wireless connectivity for the laptops in that network.

### Access Point 2

The second Access Point is connected to **Network 2** and provides wireless connectivity for the laptops in that network.

The wireless devices are connected to their corresponding Access Points and can communicate with the rest of the network through the switches and routers.

---

# 📊 Network Addressing Summary

| Network | Hosts Needed | CIDR | Subnet Mask | Usable Hosts | Network Address | Broadcast |
|---|---:|---|---|---:|---|---|
| Network 3 | 50 | `/26` | 255.255.255.192 | 62 | 192.168.1.0 | 192.168.1.63 |
| Network 4 | 50 | `/26` | 255.255.255.192 | 62 | 192.168.1.64 | 192.168.1.127 |
| Network 1 | 20 | `/27` | 255.255.255.224 | 30 | 192.168.1.128 | 192.168.1.159 |
| Network 2 | 20 | `/27` | 255.255.255.224 | 30 | 192.168.1.160 | 192.168.1.191 |
| Network 5 | 12 | `/28` | 255.255.255.240 | 14 | 192.168.1.192 | 192.168.1.207 |
| Network 6 | 12 | `/28` | 255.255.255.240 | 14 | 192.168.1.208 | 192.168.1.223 |
| Network 7 | 2 | `/30` | 255.255.255.252 | 2 | 192.168.1.224 | 192.168.1.227 |
| Network 8 | 2 | `/30` | 255.255.255.252 | 2 | 192.168.1.228 | 192.168.1.231 |
| Network 9 | 2 | `/30` | 255.255.255.252 | 2 | 192.168.1.232 | 192.168.1.235 |

---

# 🧩 Devices Summary

| Component | Quantity |
|---|---:|
| Routers | 3 |
| Switches | 6 |
| Servers | 3 |
| Access Points | 2 |
| Networks | 9 |

### Server Distribution

| Server | Network | Purpose | IP Address |
|---|---|---|---|
| DHCP Server | Network 3 | Centralized DHCP | `192.168.1.2` |
| Cisco/Web Server | Network 3 | Hosts project website | `192.168.1.10` |
| DNS Server | Network 5 | DNS name resolution | `192.168.1.195` |

---

# 🛠️ Tools & Technologies

- Cisco Packet Tracer
- IPv4 Addressing
- VLSM Subnetting
- Static Routing
- DHCP
- DHCP Relay
- `ip helper-address`
- DNS
- HTTP Web Server
- Wireless Networking
- Cisco Routers
- Cisco Switches
- Access Points

---

# 📸 Project Screenshots

## Full Network Topology

<!-- Add topology screenshot here -->

## Network Services Website

<!-- Add network services screenshot here -->

## Network Overview

<!-- Add network overview screenshot here -->

## Project Information

<!-- Add project information screenshot here -->

---

# 📁 Project File

The complete Cisco Packet Tracer project is available in this repository.

The `.pkt` file can be opened using **Cisco Packet Tracer**.

---

# 👩‍💻 Author

**Hamsa Ihab Mohamed Khairy**

Cybersecurity Student

Faculty of Computers and Data Science

Alexandria University

### Training

**NTI Network Security Training**

---

## ❤️ Acknowledgment

Special thanks to my instructor Aya Magdy for the guidance, support, and encouragement throughout the training and project.
