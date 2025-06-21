# Small-Business-Network-Simulation


## Description
This project simulates a secure small business network using Cisco Packet Tracer. It incorporates key enterprise features such as inter-VLAN routing, DHCP, NAT/PAT, wireless access, Layer 2 security, and high availability through HSRP. The network is built using a Two-Tier (Collapsed Core) Design and supports common internal services like Web, Email, FTP, and DNS.

## Scenario 
I have been hired to design and implement the network infrastructure for a small business with three departments: Administration, Sales, and IT. It is necessary to establish a Guest network to facilitate internet access for visitors. Each department will function on its own VLAN to ensure appropriate segmentation and security. The following protocols and features are implemented:
* Routing & Services: OSPF, DHCP, DNS, NAT/PAT, ICMP, NTP, Syslog
* Remote Access: SSH, HTTPS/HTTP
* Security & Control: ACLs, Port Security, BPDU Guard, Root Guard, DHCP Snooping, Dynamic ARP Inspection (DAI)

## VLAN and IP Addressing Plan
| Department     | VLAN ID | Subnet            | Gateway IP        |
|----------------|---------|-------------------|-------------------|
| Administration | 10      | 192.168.10.0/29   | 192.168.10.1      |
| Sales          | 20      | 192.168.20.0/29   | 192.168.20.1      |
| IT             | 30      | 192.168.30.0/29   | 192.168.30.1      |
| Guest          | 40      | 192.168.40.0/26   | 192.168.40.1      |
| Servers        | 50      | 192.168.50.0/28   | 192.168.50.1      |

## Utilities Used
* Cisco Packet Tracer
* Cisco CLI

## Project Walk-Through:
