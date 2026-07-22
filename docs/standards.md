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
