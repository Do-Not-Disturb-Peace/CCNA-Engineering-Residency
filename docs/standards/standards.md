# Engineering Documentation Standards

**Project:** CCNA Engineering Residency
**Version:** 2.0
**Status:** Active
**Owner:** LaToya Ellis
**Last Updated:** July 2026

---

## Purpose

This document establishes the documentation, naming, and version control standards used throughout the CCNA Engineering Residency.

The objective is to ensure every deployment is documented consistently and can be understood, reproduced, and verified by another engineer.

---

## Device Naming

- Headquarters router: `HQ-R1`
- Headquarters switches: `HQ-SW1`, `HQ-SW2`
- Dallas router: `DAL-R1`
- Austin router: `AUS-R1`
- Internet edge: `HQ-EDGE-R1`

## Files

Use lowercase or consistent Pascal-style names without spaces:

- `day01-small-office.pkt`
- `day01-topology.png`
- `hq-r1-running-config.txt`
- `verification-results.txt`

## Commit Messages

Use action-based messages:

- `Add Day 01 headquarters deployment`
- `Document VLAN troubleshooting results`
- `Update Week 02 engineering review`
- `Fix incorrect trunk configuration`

Avoid meaningless messages such as `update`, `stuff`, or `changes`.

## Evidence

Every completed deployment should contain:
- Packet Tracer file
- Ticket
- Lab report
- Topology image
- Addressing table
- Relevant device configurations
- Verification output
- Troubleshooting record
- Journal entry
- Recording link when applicable
# Lab Recording Script

**Recording Title:**
**Lab ID:**
**Related Ticket:**
**Related Lab Report:**
**Engineer:** LaToya Ellis
**Recording Date:**
**Estimated Length:** 10–15 minutes

---

# Introduction (30–60 Seconds)

Introduce yourself and the lab.

Example:

>Hello, my name is LaToya Ellis, and in this lab I'll be demonstrating the implementation of [topic]. I'll explain the business scenario, walk through the network configuration, verify connectivity, and discuss the lessons learned during the deployment.

---

# Business Scenario

Explain the problem being solved.

Cover:

- Customer requirements
- Business objective
- Technical objective
- Success criteria

---

# Network Overview

Display the topology.

Discuss:

- Devices
- IP addressing
- VLANs
- Routing
- Network services
- Security features

---

# Implementation Walkthrough

Explain each major configuration step.

## Device Preparation

Notes:

---

## Switch Configuration

Notes:

---

## Router Configuration

Notes:

---

## Routing Configuration

Notes:

---

## Security Configuration

Notes:

---

## Services Configuration

Notes:

Examples:

- DHCP
- NAT/PAT
- ACLs
- SSH
- DNS
- NTP

---

# Verification

Demonstrate validation of the deployment.

Suggested commands:

```text
show ip interface brief
show interfaces status
show vlan brief
show interfaces trunk
show ip route
show access-lists
show running-config
ping
traceroute
```

Explain:

- What command you're running
- What you're expecting to see
- Whether the result meets expectations

---

# Troubleshooting (If Needed)

If you encountered any issues, explain:

- The symptoms
- Your troubleshooting process
- Commands used
- Root cause
- Resolution

---

# Results

Summarize the outcome.

Discuss:

- Was the objective achieved?
- Did all tests pass?
- Were there any remaining issues?
- Was a rollback required?

---

# Lessons Learned

Discuss:

- New concepts learned
- Mistakes made
- Best practices discovered
- What you would do differently next time

---

# Portfolio Artifacts

Mention the supporting documentation created for this lab.

- Engineering Ticket
- Lab Report
- Change Request (if applicable)
- Daily Journal
- Network Diagram
- Configuration Backup
- GitHub Commit

---

# Key Takeaways

Summarize the three most important lessons from the lab.

1.

2.

3.

---

# Next Steps

Explain what you'll be working on next.

Examples:

- Expanding the topology
- Adding redundancy
- Implementing OSPF
- Configuring IPv6
- Strengthening network security

---

# Closing

Example:

>Thank you for watching this lab walkthrough. This project and its supporting documentation are available in my GitHub repository. I look forward to building on these concepts in the next deployment.

---

# Recording Checklist

## Before Recording

- [ ] Lab completed
- [ ] Ticket completed
- [ ] Lab Report completed
- [ ] Topology finalized
- [ ] Configurations verified
- [ ] Screenshots ready
- [ ] Notes prepared

---

## During Recording

- [ ] Speak clearly
- [ ] Explain decisions
- [ ] Show verification commands
- [ ] Describe troubleshooting
- [ ] Keep a steady pace
- [ ] Stay focused on objectives

---

## Before Publishing

- [ ] Review recording
- [ ] Confirm audio quality
- [ ] Confirm video quality
- [ ] Remove mistakes if necessary
- [ ] Verify GitHub links
- [ ] Upload recording
