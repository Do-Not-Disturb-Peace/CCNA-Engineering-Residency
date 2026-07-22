# Network Device Inventory

**Inventory ID:**
**Lab ID:**
**Related Topology:**
**Related IP Addressing Plan:**
**Related Ticket:**
**Engineer:** LaToya Ellis
**Date:**
**Version:**

---

# Inventory Overview

Provide a brief description of the devices included in this deployment.

---

# Device Summary

| Device ID | Hostname | Device Type    | Model | Role | Status |
| --------- | -------- | -------------- | ----- | ---- | :----: |
|           |          | Router         |       |      | Active |
|           |          | Layer 3 Switch |       |      | Active |
|           |          | Layer 2 Switch |       |      | Active |
|           |          | PC             |       |      | Active |
|           |          | Server         |       |      | Active |

---

# Device Details

| Hostname | Management IP | MAC Address | IOS Version | Serial Number | Physical Location |
| -------- | ------------- | ----------- | ----------- | ------------- | ----------------- |
|          |               |             |             |               |                   |

---

# Interface Inventory

| Hostname | Interface | Connected To | IP Address | VLAN | Speed | Duplex | Status |
| -------- | --------- | ------------ | ---------- | ---- | ----- | ------ | :----: |
|          |           |              |            |      |       |        |   Up   |

---

# Routing Devices

| Hostname | Routing Protocol            | Default Route | Notes |
| -------- | --------------------------- | ------------- | ----- |
|          | Static / OSPF / RIP / EIGRP | Yes / No      |       |

---

# Switching Devices

| Hostname | VLANs | Trunk Ports | Access Ports | STP Root |
| -------- | ----- | ----------- | ------------ | -------- |
|          |       |             |              | Yes / No |

---

# End Devices

| Device | User/Department | IP Address | VLAN | Connection       |
| ------ | --------------- | ---------- | ---- | ---------------- |
|        |                 |            |      | Wired / Wireless |

---

# Network Services

| Device | Service |       Status       | Notes |
| ------ | ------- | :----------------: | ----- |
|        | DHCP    | Enabled / Disabled |       |
|        | DNS     | Enabled / Disabled |       |
|        | NAT/PAT | Enabled / Disabled |       |
|        | SSH     | Enabled / Disabled |       |
|        | NTP     | Enabled / Disabled |       |
|        | Syslog  | Enabled / Disabled |       |

---

# Configuration Backup

| Device | Backup File | Backup Date | Verified |
| ------ | ----------- | ----------- | :------: |
|        |             |             | Yes / No |

---

# Maintenance History

| Date | Device | Activity | Engineer |
| ---- | ------ | -------- | -------- |
|      |        |          |          |

---

# Known Issues

| Device | Issue | Impact | Resolution |
| ------ | ----- | ------ | ---------- |
|        |       |        |            |

---

# Verification Commands

```text
show version
show inventory
show running-config
show startup-config
show ip interface brief
show interfaces status
show vlan brief
show interfaces trunk
show cdp neighbors
show lldp neighbors
```

---

# Inventory Validation Checklist

- [ ] Every device documented
- [ ] Hostnames verified
- [ ] Management IPs verified
- [ ] IOS versions recorded
- [ ] Interface assignments verified
- [ ] Routing devices documented
- [ ] Switching devices documented
- [ ] Services documented
- [ ] Configuration backups completed

---

# Related Documentation

- Network Topology
- IP Addressing Plan
- Engineering Ticket
- Change Request
- Lab Report
- Configuration Backups
- Daily Journal

---

# Revision History

| Version | Date | Author       | Changes         |
| ------- | ---- | ------------ | --------------- |
| 1.0     |      | LaToya Ellis | Initial version |
