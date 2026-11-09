# Small Business Network Segmentation Using Cisco Packet Tracer

## Project Overview

This is a networking project I built using Cisco Packet Tracer to practice network configuration and security.

The main goal is to design a small business network with two departments, HR and IT. Each department uses a separate VLAN, and a router provides communication between them.

I also configured Access Control Lists (ACLs) to restrict network access and DHCP to assign IP addresses automatically.

## Tools Used

- Cisco Packet Tracer
- Cisco 1941 Router
- Cisco 2960 Switch
- Cisco IOS CLI
- Four simulated PCs

## Network Topology

![Network Topology](screenshots/topology.png)

The network consists of one router, one switch, and four computers divided into two departments.

## Network Configuration

| Department | VLAN | Network | Gateway |
|---|---|---|---|
| HR | VLAN 10 | 192.168.10.0/24 | 192.168.10.1 |
| IT | VLAN 20 | 192.168.20.0/24 | 192.168.20.1 |

## Project Implementation

### Phase 1 — VLAN Configuration

Created VLAN 10 for HR and VLAN 20 for IT. Assigned switch ports to separate the departments into different logical networks.

### Phase 2 — Inter-VLAN Routing

Configured Router-on-a-Stick using router subinterfaces and a trunk connection to allow communication between both VLANs.

### Phase 3 — Network Security

Configured an extended ACL to block HR-initiated traffic to IT while allowing IT-initiated ping requests to HR.

This demonstrates basic traffic filtering using Cisco ACLs.

### Phase 4 — DHCP Configuration

Configured two DHCP pools on the router so that computers in each VLAN can receive IP addresses automatically.

## Network Testing

The following tests were designed to verify the network:

| Test | Expected Result |
|---|---|
| HR to HR ping | Success |
| IT to IT ping | Success |
| HR to IT ping after ACL | Blocked |
| IT to HR ping after ACL | Success |
| DHCP address assignment | Correct VLAN subnet |

Actual test screenshots are stored in the screenshots folder. The expected results above should be checked against the final simulation before the project is published.

## Project Files

- packet-tracer — Complete network simulation
- configs — Router and switch configurations
- screenshots — Network topology and verification evidence

## What I Learned

Through this project, I practiced configuring VLANs, connecting different networks using a router, applying basic network security rules, and setting up DHCP.

I also gained more experience using Cisco IOS commands and troubleshooting connectivity issues.

## Future Improvements

- Add more departments and VLANs.
- Implement additional security policies.
- Add a simulated server.
- Explore OSPF routing with multiple routers.

## Note

This project was created in a simulated environment using Cisco Packet Tracer for learning and portfolio purposes.
