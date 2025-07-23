# Small Business Network – CCNA Packet Tracer Project


## Description

This project simulates a realistic small business network using Cisco Packet Tracer, designed to demonstrate the core networking skills covered in the CCNA certification. It includes routing, VLANs, DHCP, DNS, ACLs, Syslog, wireless networking, and basic WAN redundancy.

The network is structured for scalability, security, redundancy, and highlights both Layer 2 and Layer 3 infrastructure across multiple departments.


## Key Objectives

- Build a secure, segmented business network with multiple departments
- Implement inter-VLAN routing, DHCP, DNS, and wireless access
- Configure ACLs to control traffic between departments and servers
- Simulate redundant links and basic WAN connectivity
- Collect device logs using a Syslog server
- Reinforce core CCNA concepts in a practical, hands-on environment


## Network Features

- 2 ISP routers for simulated WAN connections
- 2 core routers and 2 Layer 3 switches for routing and redundancy
- 6 Layer 2 switches, one per department and one for servers
- 5 departmental VLANs (HR, Sales, Finance, Admin, IT) with wired and wireless clients
- 1 server VLAN hosting:
  - DHCP Server
  - DNS Server
  - Syslog Server
- 3 routed links between Layer 3 switches for high availability
- Access Points in each department for wireless access


## Network Topology Diagram

Visual representation of the network layout built in Cisco Packet Tracer.

<img width="1191" height="705" alt="Network Topology Diagram" src="https://github.com/user-attachments/assets/66fc5e3f-a592-44f3-a814-9c2b409da16a" />


## VLAN & IP Addressing Plan

| VLAN ID | VLAN Name       | Department   | Subnet             | CIDR | Usable IPs | Default Gateway |
|---------|------------------|--------------|---------------------|------|------------|-----------------|
| 10      | VLAN10_IT        | IT           | 192.168.10.0        | /29  | 6          | 192.168.10.1    |
| 20      | VLAN20_HR        | HR           | 192.168.20.0        | /29  | 6          | 192.168.20.1    |
| 30      | VLAN30_SALES     | Sales        | 192.168.30.0        | /29  | 6          | 192.168.30.1    |
| 40      | VLAN40_FIN       | Finance      | 192.168.40.0        | /29  | 6          | 192.168.40.1    |
| 50      | VLAN50_ADMIN     | Admin        | 192.168.50.0        | /29  | 6          | 192.168.50.1    |
| 200     | VLAN200_SERVER   | Server VLAN  | 192.168.200.0       | /28  | 14         | 192.168.200.1   |

- VLSM is used to conserve address space while maintaining flexibility and clarity.
- /29 subnets are assigned to each department since each has exactly 3 devices (2 PCs + 1 laptop).
- The server VLAN uses a /28 subnet to accommodate 4 devices and allow room for future expansion.
- All client devices receive IP addresses via DHCP.
- Servers and gateways use static IP assignments for reliability and manageability.


## Utilities Used
* Cisco Packet Tracer
* Cisco IOS CLI


## Configuration Guide
