# Cisco-Packet-Tracer-Lab-Layer-3-Switching-VLANs-and-DHCP

## Overview
This project demonstrates a small enterprise-style network built using Cisco Packet Tracer.
The lab focuses on VLAN segmentation, Layer 3 switching, DHCP configuration and trunking between switches.

The network consists of two Layer 3 switches and several client devices distributed across multiple VLANs.
Inter-VLAN routing is handled by the primary switch, while a router provides a simulated internet gateway.

Here is a visual diagram of the finished product
![image alt]

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
![image alt](https://github.com/AidanBurkeCyb/Cisco-Packet-Tracer-Lab-Layer-3-Switching-VLANs-and-DHCP/blob/1bbe47ac4c9a28b6d4e03b3118d71753855c7e3b/Network%20Topology%20image.png)

## VLAN Design
**VLAN 10** - Internal LAN - Contains Laptop 1 and Laptop 2
![image alt](https://github.com/AidanBurkeCyb/Cisco-Packet-Tracer-Lab-Layer-3-Switching-VLANs-and-DHCP/blob/8b8f1d641bfbac2db3e73801b6b8af7677d0e04a/Switch%201%20Config.png)

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
##VLAN Segmentation
Devices were separated into different VLANs to simulate network segmentation and reduce broadcast domains.
##Inter-VLAN Routing
Switch 1 performs routing between VLAN 10 and VLAN 20 using Switch Virtual Interfaces (SVIs).
##DHCP Services
Switch 1 acts as a DHCP server, automatically assigning IP addresses to hosts within each VLAN.
##Trunk Link Between Switches
A trunk connection between the switches allows VLAN 20 to span both switches, enabling devices on different switches to remain in the same broadcast domain.
##Internet Gateway
A router connected to Switch 1 provides a simulated upstream connection to the internet.

# Network Verification
The network was tested to confirm correct functionality:
Devices successfully received IP addresses via DHCP
	![image alt](https://github.com/AidanBurkeCyb/Cisco-Packet-Tracer-Lab-Layer-3-Switching-VLANs-and-DHCP/blob/bd23d02267a9ac2e6a655cf76c998df72a5d6f83/DHCDP%20Laptop%201.png)
	![image alt](https://github.com/AidanBurkeCyb/Cisco-Packet-Tracer-Lab-Layer-3-Switching-VLANs-and-DHCP/blob/bd23d02267a9ac2e6a655cf76c998df72a5d6f83/DHCP%20Laptop%202.png)
	![image alt](https://github.com/AidanBurkeCyb/Cisco-Packet-Tracer-Lab-Layer-3-Switching-VLANs-and-DHCP/blob/bd23d02267a9ac2e6a655cf76c998df72a5d6f83/DHCP%20Laptop%203.png)
	![image alt](https://github.com/AidanBurkeCyb/Cisco-Packet-Tracer-Lab-Layer-3-Switching-VLANs-and-DHCP/blob/bd23d02267a9ac2e6a655cf76c998df72a5d6f83/DHCP%20Laptop%204.png)
	![image alt](https://github.com/AidanBurkeCyb/Cisco-Packet-Tracer-Lab-Layer-3-Switching-VLANs-and-DHCP/blob/bd23d02267a9ac2e6a655cf76c998df72a5d6f83/DHCP%20Laptop%205.png)

Inter-VLAN routing allowed communication between VLAN 10 and VLAN 20

![image alt](https://github.com/AidanBurkeCyb/Cisco-Packet-Tracer-Lab-Layer-3-Switching-VLANs-and-DHCP/blob/a98b093c62756c2a20fd00d770d2321abe181246/Ping%20Test%20VLAN%202%20-%3E%20VLAN%201.png)
	
Hosts were able to reach the gateway router
![image alt](https://github.com/AidanBurkeCyb/Cisco-Packet-Tracer-Lab-Layer-3-Switching-VLANs-and-DHCP/blob/d4b5719f974f0e76e9ad57968943ecd84ec55d88/Pinging%20Router%20from%20VLAN%2010.png)
![image alt](https://github.com/AidanBurkeCyb/Cisco-Packet-Tracer-Lab-Layer-3-Switching-VLANs-and-DHCP/blob/d4b5719f974f0e76e9ad57968943ecd84ec55d88/Pinging%20Router%20from%20Device%20in%20VLAN%2020.png)

# Skills Demonstrated
	•	VLAN configuration
	•	Layer 3 switching
	•	Inter-VLAN routing
	•	DHCP server configuration
	•	802.1Q trunking
	•	Network segmentation
	•	Basic routing configuration
	•	Troubleshooting connectivity issues

# Files Included
	•	Packet Tracer lab file (.pkt)
	•	Network topology diagram
	•	Switch and router configuration exports

# Configuration files were exported using:
show running-config

