# CCNA Enterprise Network Project

## Overview
This project is a Cisco Packet Tracer enterprise-style network built to demonstrate core CCNA networking concepts in a practical topology. The network includes a headquarters environment with multiple departmental VLANs, a branch office, dynamic routing between sites, NAT to an ISP-facing network, and several switch security features.

## Topology Summary
The topology includes:
- 2 Cisco 2911 routers
- 3 Cisco 2960 switches
- Multiple end devices across different departments
- A simulated ISP connection
- A public server network

### Network Segments
- VLAN 10: IT
- VLAN 20: Sales
- VLAN 30: HR
- VLAN 99: Management
- Branch LAN: 10.20.20.0/26
- WAN link between R1 and R2: 10.0.0.0/30
- ISP-facing link: 203.0.113.0/30

## Implemented Features
- Router-on-a-stick inter-VLAN routing
- OSPF dynamic routing between HQ and branch
- DHCP for multiple internal networks
- NAT overload (PAT) for internal-to-public connectivity
- SSH-only remote management
- Access control list to restrict HR-to-IT host access
- Switch port security using sticky MAC addresses
- DHCP snooping
- Dynamic ARP Inspection (DAI)
- Spanning Tree PortFast and BPDU Guard
- Management VLAN for switch administration

## Devices

### Routers
- R1: HQ router, inter-VLAN routing, DHCP, NAT, OSPF
- R2: Branch router, DHCP, OSPF

### Switches
- SW1: Main HQ access/distribution switch
- SW2: HR access switch
- SW3: Branch access switch

## Verification Performed
The following were verified from CLI output:
- OSPF neighbor adjacency between R1 and R2
- OSPF route learning for remote networks
- Default route propagation from HQ to branch
- Active VLAN assignments on switches
- Trunk links carrying VLAN traffic
- Operational router interfaces in up/up state

## Project Structure
- `topology.pkt` contains the Packet Tracer topology
- `configs/` contains running configurations for routers and switches
- `verification/` contains CLI proof of routing, VLANs, trunking, and interface status
- `images/` contains topology screenshots

## Notes
This project was built as a practical CCNA lab to demonstrate routing, switching, segmentation, and basic network hardening. Some areas could be further refined, such as standardizing management design across all switches and tightening trunk allowed VLAN settings.

## How to Use
1. Open the `.pkt` file in Cisco Packet Tracer
2. Review the device configurations in the `configs/` folder
3. Check the `verification/` folder for proof of routing and switching behavior
4. Use the topology image for a quick visual overview

## Skills Demonstrated
- IP addressing and subnetting
- VLAN creation and segmentation
- Inter-VLAN routing
- OSPF configuration and verification
- NAT/PAT
- DHCP configuration
- ACL configuration
- Switch security hardening
- Network verification and troubleshooting
