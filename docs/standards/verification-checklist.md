# Network Verification Checklist

**Verification ID:**
**Lab ID:**
**Related Ticket:**
**Related Change Request:**
**Related Lab Report:**
**Engineer:** LaToya Ellis
**Date:**

---

# Purpose

This checklist defines the standard validation process performed after implementing a network change. Completing each section helps confirm that the deployment functions as expected and that documentation is complete.

---

# Device Health

| Verification Item              |    Status     | Notes |
| ------------------------------ | :-----------: | ----- |
| Devices powered on             | ☐ Pass ☐ Fail |       |
| Hostnames verified             | ☐ Pass ☐ Fail |       |
| IOS version verified           | ☐ Pass ☐ Fail |       |
| Running configuration reviewed | ☐ Pass ☐ Fail |       |
| Startup configuration saved    | ☐ Pass ☐ Fail |       |

---

# Interface Verification

| Verification Item                 |    Status     | Notes |
| --------------------------------- | :-----------: | ----- |
| All required interfaces are up    | ☐ Pass ☐ Fail |       |
| Interface descriptions configured | ☐ Pass ☐ Fail |       |
| Speed and duplex correct          | ☐ Pass ☐ Fail |       |
| No unexpected interface errors    | ☐ Pass ☐ Fail |       |

Recommended Commands

```text
show ip interface brief
show interfaces
show interfaces status
```

---

# VLAN Verification

| Verification Item               |    Status     | Notes |
| ------------------------------- | :-----------: | ----- |
| VLANs created                   | ☐ Pass ☐ Fail |       |
| Access ports assigned correctly | ☐ Pass ☐ Fail |       |
| Native VLAN verified            | ☐ Pass ☐ Fail |       |

Recommended Commands

```text
show vlan brief
show interfaces switchport
```

---

# Trunk Verification

| Verification Item       |    Status     | Notes |
| ----------------------- | :-----------: | ----- |
| Trunk links operational | ☐ Pass ☐ Fail |       |
| Allowed VLANs verified  | ☐ Pass ☐ Fail |       |
| Native VLAN consistent  | ☐ Pass ☐ Fail |       |

Recommended Commands

```text
show interfaces trunk
```

---

# Spanning Tree Verification

| Verification Item                     |    Status     | Notes |
| ------------------------------------- | :-----------: | ----- |
| Root bridge verified                  | ☐ Pass ☐ Fail |       |
| PortFast configured where appropriate | ☐ Pass ☐ Fail |       |
| BPDU Guard enabled on access ports    | ☐ Pass ☐ Fail |       |

Recommended Commands

```text
show spanning-tree
```

---

# EtherChannel Verification (If Applicable)

| Verification Item         |    Status     | Notes |
| ------------------------- | :-----------: | ----- |
| Port channel formed       | ☐ Pass ☐ Fail |       |
| Member interfaces bundled | ☐ Pass ☐ Fail |       |

Recommended Commands

```text
show etherchannel summary
```

---

# Routing Verification

| Verification Item             |    Status     | Notes |
| ----------------------------- | :-----------: | ----- |
| Routes installed              | ☐ Pass ☐ Fail |       |
| Default route present         | ☐ Pass ☐ Fail |       |
| Dynamic neighbors established | ☐ Pass ☐ Fail |       |

Recommended Commands

```text
show ip route
show ip ospf neighbor
```

---

# Network Services

| Service |    Status     | Notes |
| ------- | :-----------: | ----- |
| DHCP    | ☐ Pass ☐ Fail |       |
| NAT/PAT | ☐ Pass ☐ Fail |       |
| DNS     | ☐ Pass ☐ Fail |       |
| SSH     | ☐ Pass ☐ Fail |       |
| NTP     | ☐ Pass ☐ Fail |       |

Recommended Commands

```text
show ip dhcp binding
show ip nat translations
show ip ssh
show clock
```

---

# Security Verification

| Verification Item            |    Status     | Notes |
| ---------------------------- | :-----------: | ----- |
| Enable secret configured     | ☐ Pass ☐ Fail |       |
| Local user accounts verified | ☐ Pass ☐ Fail |       |
| SSH only (no Telnet)         | ☐ Pass ☐ Fail |       |
| ACLs functioning as expected | ☐ Pass ☐ Fail |       |
| Unused ports shut down       | ☐ Pass ☐ Fail |       |

Recommended Commands

```text
show running-config
show access-lists
```

---

# Connectivity Testing

| Test                 | Expected Result | Actual Result |    Status     |
| -------------------- | --------------- | ------------- | :-----------: |
| Ping default gateway | Success         |               | ☐ Pass ☐ Fail |
| Ping remote VLAN     | Success         |               | ☐ Pass ☐ Fail |
| Ping server          | Success         |               | ☐ Pass ☐ Fail |
| Traceroute           | Expected path   |               | ☐ Pass ☐ Fail |

---

# Performance Validation

| Verification Item             |    Status     | Notes |
| ----------------------------- | :-----------: | ----- |
| No excessive interface errors | ☐ Pass ☐ Fail |       |
| Low latency observed          | ☐ Pass ☐ Fail |       |
| No packet loss detected       | ☐ Pass ☐ Fail |       |

---

# Documentation Verification

- [ ] Topology updated
- [ ] IP Addressing Plan updated
- [ ] Device Inventory updated
- [ ] Engineering Ticket completed
- [ ] Change Request completed (if applicable)
- [ ] Lab Report completed
- [ ] Daily Journal completed
- [ ] Screenshots captured
- [ ] Configuration backups saved

---

# Evidence Collected

- [ ] Running Configuration
- [ ] Startup Configuration
- [ ] Verification Command Output
- [ ] Packet Tracer File
- [ ] Network Diagram
- [ ] Screenshots
- [ ] Git Commit
- [ ] Video Recording

---

# Final Validation

Overall Deployment Status

- ☐ Successful
- ☐ Successful with Minor Issues
- ☐ Failed
- ☐ Rolled Back

---

# Engineer Sign-Off

**Engineer:**

**Verification Date:**

**Comments:**

---

# Lessons Learned

-
-
-

---

# Related Documentation

- Network Topology
- IP Addressing Plan
- Device Inventory
- Engineering Ticket
- Change Request
- Lab Report
- Daily Journal
- Weekly Review

---

# Revision History

| Version | Date | Author       | Changes         |
| ------- | ---- | ------------ | --------------- |
| 1.0     |      | LaToya Ellis | Initial version |
