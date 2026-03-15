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
                Internet
                   |
                Router
                   |
                Switch1
            ┌─────────────┐
 Laptop1 ───┤ Fa0/2 VLAN10│
 Laptop2 ───┤ Fa0/3 VLAN10│
 Laptop3 ───┤ Fa0/4 VLAN20│
            │             │
            │ Gi0/1       │
            └─────┬───────┘
                  │ trunk
                  │
             Switch2
            ┌─────────────┐
 Laptop4 ───┤ Fa0/2 VLAN20│
 Laptop5 ───┤ Fa0/3 VLAN20│

 Network Diagram with IPs.png

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

# Key Features Implemented

VLAN Segmentation
Devices were separated into different VLANs to simulate network segmentation and reduce broadcast domains.

Inter-VLAN Routing
Switch 1 performs routing between VLAN 10 and VLAN 20 using Switch Virtual Interfaces (SVIs).

DHCP Services
Switch 1 acts as a DHCP server, automatically assigning IP addresses to hosts within each VLAN.

Trunk Link Between Switches
A trunk connection between the switches allows VLAN 20 to span both switches, enabling devices on different switches to remain in the same broadcast domain.

Internet Gateway
A router connected to Switch 1 provides a simulated upstream connection to the internet.

# Network Verification

The network was tested to confirm correct functionality:
	•	Devices successfully received IP addresses via DHCP
	•	Devices in VLAN 20 could communicate across both switches
	•	Inter-VLAN routing allowed communication between VLAN 10 and VLAN 20
	•	Hosts were able to reach the gateway router

Skills Demonstrated
	•	VLAN configuration
	•	Layer 3 switching
	•	Inter-VLAN routing
	•	DHCP server configuration
	•	802.1Q trunking
	•	Network segmentation
	•	Basic routing configuration
	•	Troubleshooting connectivity issues
