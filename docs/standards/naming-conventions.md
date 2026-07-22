# Network Engineering Naming Conventions

**Repository:** CCNA-Engineering-Residency
**Engineer:** LaToya Ellis
**Version:** 1.0
**Effective Date:**

---

# Purpose

This document establishes the naming standards used throughout this repository. Consistent naming improves readability, troubleshooting, documentation quality, and maintainability across every lab and project.

---

# Hostname Standards

## Routers

Format:

```text
R-<Site>-<Number>
```

Examples:

```text
R-HQ-01
R-BR1-01
R-BR2-01
```

---

## Layer 3 Switches

Format:

```text
L3SW-<Site>-<Number>
```

Examples:

```text
L3SW-HQ-01
L3SW-BR1-01
```

---

## Layer 2 Switches

Format:

```text
SW-<Site>-<Number>
```

Examples:

```text
SW-HQ-01
SW-HQ-02
SW-BR1-01
```

---

## Wireless Access Points

Format:

```text
AP-<Site>-<Number>
```

Examples:

```text
AP-HQ-01
AP-BR1-01
```

---

## Firewalls

Format:

```text
FW-<Site>-<Number>
```

Examples:

```text
FW-HQ-01
```

---

## Servers

Format:

```text
SRV-<Function>-<Number>
```

Examples:

```text
SRV-DHCP-01
SRV-DNS-01
SRV-WEB-01
SRV-FILE-01
```

---

## End Devices

Format:

```text
PC-<Department>-<Number>
```

Examples:

```text
PC-HR-01
PC-IT-01
PC-SALES-01
```

---

# Site Naming

| Site            | Code |
| --------------- | ---- |
| Headquarters    | HQ   |
| Branch Office 1 | BR1  |
| Branch Office 2 | BR2  |
| Branch Office 3 | BR3  |
| Data Center     | DC   |

---

# VLAN Naming

| VLAN | Name        |
| ---: | ----------- |
|   10 | Management  |
|   20 | IT          |
|   30 | HR          |
|   40 | Sales       |
|   50 | Guest       |
|   99 | Native      |
|  999 | Parking Lot |

---

# Interface Description Standard

Format:

```text
<Connected Device> | <Connected Interface>
```

Examples:

```text
SW-HQ-01 | G0/1
R-HQ-01 | G0/0
SRV-DHCP-01 | NIC1
```

---

# IP Addressing Standard

| Network       | Purpose    |
| ------------- | ---------- |
| 10.0.0.0/24   | Management |
| 10.10.10.0/24 | VLAN 10    |
| 10.20.20.0/24 | VLAN 20    |
| 10.30.30.0/24 | VLAN 30    |
| 10.40.40.0/24 | VLAN 40    |
| 10.50.50.0/24 | VLAN 50    |

Guidelines:

- First usable IP = Default gateway
- Second usable IP = Infrastructure device
- Servers use static IP addresses
- Client devices use DHCP unless otherwise required
- Reserve address ranges for future growth

---

# Configuration File Naming

Format:

```text
<Hostname>-running-config.txt
```

Examples:

```text
R-HQ-01-running-config.txt
SW-HQ-01-running-config.txt
```

---

# Packet Tracer File Naming

Format:

```text
LabXX-Short-Description.pkt
```

Examples:

```text
Lab01-Basic-Switching.pkt
Lab02-VLAN-Configuration.pkt
Lab10-OSPF.pkt
```

---

# Network Diagram Naming

Format:

```text
LabXX-Topology.png
```

Examples:

```text
Lab01-Topology.png
Lab05-Topology.png
```

---

# Screenshot Naming

Format:

```text
LabXX-Description.png
```

Examples:

```text
Lab03-Ping-Test.png
Lab07-VLAN-Verification.png
Lab12-OSPF-Neighbors.png
```

---

# Documentation Naming

Format:

```text
lab-report.md
engineering-ticket.md
daily-journal.md
weekly-review.md
change-request.md
```

---

# Git Branch Naming

Format:

```text
feature/<topic>
bugfix/<issue>
docs/<topic>
```

Examples:

```text
feature/vlan-lab
feature/ospf
docs/topology-template
bugfix/interface-labels
```

---

# Git Commit Message Standard

Format:

```text
<type>: <description>
```

Types:

- feat
- fix
- docs
- refactor
- chore

Examples:

```text
feat: add VLAN topology
docs: create device inventory template
fix: correct OSPF configuration
refactor: simplify router baseline config
chore: update repository structure
```

---

# Folder Structure Standard

```text
CCNA-Engineering-Residency/
│
├── docs/
├── templates/
├── labs/
├── configs/
├── diagrams/
├── screenshots/
├── recordings/
└── images/
```

---

# General Standards

- Use meaningful, descriptive names.
- Keep naming consistent across all labs.
- Avoid spaces in filenames; use hyphens instead.
- Use uppercase for device hostnames.
- Use lowercase for Markdown filenames.
- Include interface descriptions where supported.
- Update documentation whenever topology or addressing changes.

---

# Revision History

| Version | Date | Author       | Changes         |
| ------- | ---- | ------------ | --------------- |
| 1.0     |      | LaToya Ellis | Initial version |

