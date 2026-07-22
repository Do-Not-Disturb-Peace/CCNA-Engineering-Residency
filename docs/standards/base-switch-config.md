# Cisco IOS Base Switch Configuration Standard

**Repository:** CCNA-Engineering-Residency
**Engineer:** LaToya Ellis
**Version:** 1.0

---

# Purpose

This document defines the standard baseline configuration for Cisco Layer 2 switches used throughout this residency. Applying the same baseline to every switch improves consistency, security, troubleshooting, and documentation while reflecting enterprise deployment practices.

---

# Base Configuration

```cisco
enable
configure terminal

! Hostname
hostname SW-HQ-01

! Disable DNS lookup
no ip domain-lookup

! Secure privileged EXEC mode
enable secret <SET_SECURE_PASSWORD>

! Encrypt plaintext passwords
service password-encryption

! Password requirements
security passwords min-length 10

! Login banner
banner motd ^
************************************************
* Authorized Access Only                      *
* Unauthorized access is prohibited.          *
************************************************
^

! Local administrator
username admin privilege 15 secret <SET_SECURE_PASSWORD>

! Domain name
ip domain-name lab.local

! Generate RSA keys
crypto key generate rsa modulus 2048

! Enable SSH Version 2
ip ssh version 2

! Console configuration
line console 0
 logging synchronous
 exec-timeout 10 0
 login local
 exit

! VTY configuration
line vty 0 15
 login local
 transport input ssh
 exec-timeout 10 0
 exit

! Disable HTTP services
no ip http server
no ip http secure-server

! Management VLAN
interface vlan 10
 description Management VLAN
 ip address 10.10.10.2 255.255.255.0
 no shutdown
 exit

! Default gateway
ip default-gateway 10.10.10.1

end

copy running-config startup-config
```

---

# Configuration Breakdown

## Hostname

```cisco
hostname SW-HQ-01
```

Assign a hostname that follows the repository naming convention.

---

## Disable DNS Lookup

```cisco
no ip domain-lookup
```

Prevents unnecessary delays when mistyped commands are entered.

---

## Enable Secret

```cisco
enable secret <SET_SECURE_PASSWORD>
```

Protects privileged EXEC mode using an encrypted password.

---

## Password Encryption

```cisco
service password-encryption
```

Encrypts passwords stored in the configuration.

---

## Local User Account

```cisco
username admin privilege 15 secret <SET_SECURE_PASSWORD>
```

Creates the local administrative account used for console and SSH authentication.

---

## SSH Configuration

```cisco
ip domain-name lab.local
crypto key generate rsa modulus 2048
ip ssh version 2
```

Enables secure remote administration using SSH.

---

## Management VLAN

```cisco
interface vlan 10
 ip address 10.10.10.2 255.255.255.0
 no shutdown
```

Provides a dedicated management interface for the switch.

---

## Default Gateway

```cisco
ip default-gateway 10.10.10.1
```

Allows the switch to communicate with devices outside its local subnet.

---

# Access Port Template

```cisco
interface FastEthernet0/1

 description PC-HR-01

 switchport mode access

 switchport access vlan 30

 spanning-tree portfast

 spanning-tree bpduguard enable

 no shutdown
```

Use this template for end-device connections.

---

# Trunk Port Template

```cisco
interface GigabitEthernet0/1

 description Uplink to R-HQ-01

 switchport mode trunk

 switchport trunk native vlan 99

 switchport trunk allowed vlan 10,20,30,40,50,99

 no shutdown
```

Use this template for switch-to-switch or switch-to-router uplinks.

---

# Unused Ports

```cisco
interface range FastEthernet0/10-24

 description UNUSED

 shutdown
```

Disable unused ports to reduce unnecessary exposure.

---

# Port Security (Optional)

```cisco
interface FastEthernet0/1

 switchport port-security

 switchport port-security maximum 2

 switchport port-security violation restrict

 switchport port-security mac-address sticky
```

Apply when learning or demonstrating Layer 2 security concepts.

---

# Verification Commands

```cisco
show running-config

show startup-config

show interfaces status

show vlan brief

show interfaces trunk

show spanning-tree

show port-security

show mac address-table

show ip interface brief

show version
```

---

# Security Best Practices

- Use SSH instead of Telnet.
- Configure meaningful interface descriptions.
- Shut down unused interfaces.
- Enable PortFast only on access ports.
- Enable BPDU Guard on access ports.
- Use a dedicated management VLAN.
- Save the configuration after validation.
- Document all changes.

---

# Lab Customization

Update these values for each deployment.

| Setting                | Example                 |
| ---------------------- | ----------------------- |
| Hostname               | SW-BR1-01               |
| Management IP          | 10.20.20.2              |
| Default Gateway        | 10.20.20.1              |
| Management VLAN        | 10                      |
| Interface Descriptions | Match connected devices |

---

# Baseline Validation Checklist

- [ ] Hostname configured
- [ ] DNS lookup disabled
- [ ] Enable secret configured
- [ ] Password encryption enabled
- [ ] Local administrator created
- [ ] MOTD banner configured
- [ ] SSH Version 2 enabled
- [ ] RSA keys generated
- [ ] Console secured
- [ ] VTY secured
- [ ] Management VLAN configured
- [ ] Default gateway configured
- [ ] Interface descriptions added
- [ ] Unused ports shut down
- [ ] PortFast configured on access ports
- [ ] BPDU Guard configured on access ports
- [ ] Configuration saved
- [ ] Verification completed

---

# Related Documentation

- Naming Conventions
- Device Inventory
- IP Addressing Plan
- Engineering Ticket
- Lab Report
- Verification Checklist

---

# Revision History

| Version | Date | Author       | Changes         |
| ------- | ---- | ------------ | --------------- |
| 1.0     |      | LaToya Ellis | Initial version |
