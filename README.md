# Secure Enterprise Network Design

## Overview

This project demonstrates the design and implementation of a secure enterprise network using Cisco Packet Tracer.

The network is divided into three departments:

* HR (VLAN 10)
* Finance (VLAN 20)
* IT (VLAN 30)

The project implements network segmentation, DHCP services, inter-VLAN routing, and ACL-based security policies.

## Technologies

* Cisco Packet Tracer
* Cisco IOS
* VLANs
* Router-on-a-Stick
* DHCP
* Access Control Lists (ACLs)

## Network Design

### VLAN Structure

| Department | VLAN | Network         |
| ---------- | ---- | --------------- |
| HR         | 10   | 192.168.10.0/24 |
| Finance    | 20   | 192.168.20.0/24 |
| IT         | 30   | 192.168.30.0/24 |

### Router Interfaces

| Interface | IP Address   |
| --------- | ------------ |
| G0/0/0.10 | 192.168.10.1 |
| G0/0/0.20 | 192.168.20.1 |
| G0/0/0.30 | 192.168.30.1 |

## Security Policy

ACL 100 was implemented to restrict communication between departments.

* HR cannot access Finance.
* IT is allowed to communicate with all departments.

### ACL Configuration

access-list 100 deny ip 192.168.10.0 0.0.0.255 192.168.20.0 0.0.0.255

access-list 100 permit ip any any

## Validation

The following tests were successfully completed:

* DHCP address assignment
* VLAN connectivity
* Inter-VLAN routing
* ACL enforcement
* Connectivity troubleshooting

## Author

Oun Rithi

