# IP Addressing Plan

**Addressing Plan ID:**
**Lab ID:**
**Related Topology:**
**Related Ticket:**
**Engineer:** LaToya Ellis
**Date:**
**Version:**

---

# Addressing Overview

Provide a brief description of the addressing strategy used for this network.

---

# IPv4 Network Summary

| Network Name | Network Address | CIDR | Subnet Mask | Default Gateway | Purpose |
| ------------ | --------------- | ---- | ----------- | --------------- | ------- |
|              |                 |      |             |                 |         |

---

# VLAN Addressing

| VLAN ID | VLAN Name | Network | CIDR | Gateway |   DHCP   | Notes |
| ------: | --------- | ------- | ---- | ------- | :------: | ----- |
|         |           |         |      |         | Yes / No |       |

---

# Device Address Assignments

| Device | Hostname | Interface | IPv4 Address | CIDR | Default Gateway | Assignment    |
| ------ | -------- | --------- | ------------ | ---- | --------------- | ------------- |
|        |          |           |              |      |                 | Static / DHCP |

---

# DHCP Scope Plan

| Scope Name | Network | Start Address | End Address | Excluded Addresses |
| ---------- | ------- | ------------- | ----------- | ------------------ |
|            |         |               |             |                    |

---

# Static IP Reservations

| Device | IP Address | Reason |
| ------ | ---------- | ------ |
|        |            |        |

---

# IPv6 Addressing (If Applicable)

| Device | Interface | IPv6 Address | Prefix Length | Gateway |
| ------ | --------- | ------------ | ------------- | ------- |
|        |           |              |               |         |

---

# Interface Summary

| Device | Interface | Connected To | IPv4 | IPv6 | Status    |
| ------ | --------- | ------------ | ---- | ---- | --------- |
|        |           |              |      |      | Up / Down |

---

# Subnet Utilization

| Network | Total Hosts | Used | Available | Utilization |
| ------- | ----------: | ---: | --------: | ----------: |
|         |             |      |           |             |

---

# Addressing Standards

Document any standards used for assigning addresses.

Examples:

- Infrastructure devices use the first available addresses.
- Default gateways use the first usable IP.
- Servers use static addresses.
- End-user devices receive DHCP addresses.
- Management interfaces use a dedicated management subnet.

---

# Reserved Networks

| Network | Purpose |
| ------- | ------- |
|         |         |

---

# Validation Checklist

- [ ] All devices have unique IP addresses
- [ ] Subnet masks verified
- [ ] Default gateways verified
- [ ] DHCP scopes configured correctly
- [ ] Static assignments documented
- [ ] IPv6 addressing verified (if used)
- [ ] No overlapping networks
- [ ] Addressing matches topology documentation

---

# Verification Commands

```text
show ip interface brief
show running-config
show ip route
show dhcp binding
show ipv6 interface brief
ping
traceroute
```

---

# Related Documentation

- Network Topology
- Device Inventory
- Engineering Ticket
- Change Request
- Lab Report
- Configuration Backup

---

# Revision History

| Version | Date | Author       | Changes         |
| ------- | ---- | ------------ | --------------- |
| 1.0     |      | LaToya Ellis | Initial version |

