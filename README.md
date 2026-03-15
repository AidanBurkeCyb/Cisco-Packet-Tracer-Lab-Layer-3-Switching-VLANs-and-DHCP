# Cisco-Packet-Tracer-Lab-Layer-3-Switching-VLANs-and-DHCP

## Overview
This project demonstrates a small enterprise-style network built using Cisco Packet Tracer.
The lab focuses on VLAN segmentation, Layer 3 switching, DHCP configuration and trunking between switches.

The network consists of two Layer 3 switches and several client devices distributed across multiple VLANs.
Inter-VLAN routing is handled by the primary switch, while a router provides a simulated internet gateway.

## Network Topology
The network contains:
	•	1 Router
	•	2 Layer 3 Switches
	•	5 Client Laptops

Switch 1 acts as the core switch, performing:
	•	Inter-VLAN routing
	•	DHCP services
	•	Upstream routing to the router

Switch 2 extends connectivity for devices in the shared VLAN.

## Topology Diagram

## VLAN Design
**VLAN 10** - Internal LAN - Contains Laptop 1 and Laptop 2
**VLAN 20** - Shared VLAN across both switches - Laptop 3, Laptop 4 and Laptop 5

## IP Adressing plan
## VLAN 10
Network: 192.168.10.0/24
Gateway: 192.168.10.1
## VLAN 20
Network: 192.168.20.0/24
Gateway: 192.168.20.1
## Router Uplink
Network: 10.0.0.0/30
Router: 10.0.0.1
Switch1: 10.0.0.2

