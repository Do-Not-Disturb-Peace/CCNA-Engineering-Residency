# 60-Day Real-World Deployment Roadmap

This roadmap is organized by deployment outcomes. Exact Official Cert Guide chapter numbers depend on the edition. Use the listed topic titles to locate the matching chapters in your volumes. Kevin Wallace assignments should be selected by the same topic names in the course curriculum.

## Phase 0 — Workspace Preparation

### Before Day 1
- Create and clone the GitHub repository.
- Configure VS Code, Git, Packet Tracer, OBS Studio, and diagrams.net.
- Confirm access to both OCG volumes and Kevin Wallace course files.
- Test one Markdown preview, one Git commit, and one 60-second recording.

## Phase 1 — Network Technician: Headquarters Foundation

### Days 1–3: New Headquarters Equipment Deployment
OCG: Cisco IOS CLI, device management, switch interfaces, router interfaces, Ethernet LAN fundamentals  
Kevin Wallace: IOS navigation, foundational device configuration, interface configuration  
Deployment: One router, one switch, three clients, secure management  
Labs: Base configurations, SSH, CDP/LLDP, verification

### Days 4–6: IPv4 Addressing and Subnet Deployment
OCG: IPv4 addressing, subnetting, ARP, ICMP, static routes  
Kevin Wallace: IPv4 addressing, subnetting, routing fundamentals  
Deployment: Multiple small LANs connected through routers  
Labs: Address plans, gateway configuration, static routing, failure isolation

### Day 7: Promotion Project 1
Build and troubleshoot a small office network without step-by-step commands.

## Phase 2 — Junior Network Administrator: Department Segmentation

### Days 8–11: Department VLAN Deployment
OCG: VLAN concepts, access ports, switch management, voice and data VLAN concepts  
Kevin Wallace: VLAN configuration and verification  
Deployment: Accounting, HR, Sales, IT, and Management segments  
Included labs: VLAN Lab

### Days 12–14: Trunk and Inter-VLAN Deployment
OCG: 802.1Q trunking, native VLAN, router-on-a-stick, Layer 3 switching concepts  
Kevin Wallace: Trunking and inter-VLAN routing  
Deployment: Multi-department connectivity with controlled routing  
Included labs: Trunking Lab

### Days 15–18: Redundant Switching Deployment
OCG: STP, RSTP, root bridge selection, PortFast, BPDU Guard  
Kevin Wallace: Spanning Tree operations and troubleshooting  
Deployment: Two-switch redundant headquarters  
Included labs: Spanning Tree Protocol Lab

### Days 19–21: Link Aggregation Deployment
OCG: EtherChannel, LACP, PAgP, Layer 2 verification  
Kevin Wallace: EtherChannel configuration and troubleshooting  
Deployment: Increased bandwidth and redundancy between switches  
Included labs: EtherChannel Lab

### Day 22: Promotion Project 2
Deploy a segmented, redundant headquarters LAN from business requirements.

## Phase 3 — Network Engineer: Branch Connectivity

### Days 23–26: Branch Office Static Routing
OCG: Connected routes, static routes, default routes, route selection  
Kevin Wallace: Static and default routing  
Deployment: Houston headquarters and Dallas branch

### Days 27–31: OSPF Enterprise Routing
OCG: OSPF concepts, neighbor relationships, router ID, cost, passive interfaces, default route advertisement  
Kevin Wallace: Single-area OSPF configuration and troubleshooting  
Deployment: Dynamic routing between headquarters and branch sites  
Included labs: OSPF Lab

### Days 32–34: IPv6 Dual-Stack Deployment
OCG: IPv6 addressing, NDP, SLAAC, static IPv6 routing  
Kevin Wallace: IPv6 fundamentals and configuration  
Deployment: Dual-stack headquarters and branch connectivity

### Day 35: Promotion Project 3
Build a dual-site routed network and repair introduced OSPF and addressing faults.

## Phase 4 — Network Security and Internet Services

### Days 36–38: DHCP Service Deployment
OCG: DHCP concepts, relay, client address assignment  
Kevin Wallace: DHCP configuration and troubleshooting  
Included labs: DHCP Lab

### Days 39–42: NAT and Internet Edge Deployment
OCG: Static NAT, dynamic NAT, PAT, inside and outside interfaces  
Kevin Wallace: NAT and PAT  
Included labs: Static NAT, Dynamic NAT, PAT

### Days 43–47: Access Control Deployment
OCG: Standard ACLs, extended ACLs, named ACLs, placement rules, wildcard masks  
Kevin Wallace: ACL logic, configuration, and troubleshooting  
Included labs: Standard Numbered ACL, Extended Numbered ACL, Extended Named ACL

### Days 48–49: Infrastructure Management
OCG: NTP, syslog concepts, SNMP concepts, DNS overview, SSH management  
Kevin Wallace: Management and infrastructure services  
Included labs: NTP, CDP and LLDP

### Day 50: Promotion Project 4
Secure a branch Internet edge and enforce department access requirements.

## Phase 5 — Operations, Troubleshooting, and Automation Awareness

### Days 51–53: Wireless and Security Operations
OCG: Wireless architecture, WLAN security, switch port security, DHCP snooping and DAI concepts  
Kevin Wallace: Wireless and Layer 2 security topics  
Deployment: Corporate and guest wireless design and security review

### Days 54–56: Network Automation Foundations
OCG: JSON, REST APIs, controllers, SDN, configuration management, automation concepts  
Kevin Wallace: Automation and programmability  
Deployment: Document which repetitive tasks should be automated  
Optional Python: Begin Python Essentials 1 only after daily CCNA work is complete

### Days 57–59: Final Enterprise Deployment
Build a multi-site network containing VLANs, trunks, STP, EtherChannel, OSPF, IPv4, IPv6, DHCP, NAT/PAT, ACLs, NTP, SSH, and verification evidence.

### Day 60: Final Presentation and Portfolio Release
- Record a polished enterprise-network walkthrough.
- Complete the final project report.
- Clean repository structure.
- Publish selected diagrams and recordings.
- Update GitHub README.
- Add project to LinkedIn Featured.
- Publish final LinkedIn post.

## Time Allocation

- Packet Tracer and troubleshooting: 50%
- Official Cert Guide: 25%
- Kevin Wallace course: 15%
- Documentation, GitHub, and recordings: 10%

## Weekly Rhythm

- Monday–Thursday: New deployments
- Friday: Troubleshooting and engineering journal review
- Saturday: Weekly capstone or change window
- Sunday: Review, portfolio cleanup, and limited practice testing
