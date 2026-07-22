# Cisco IOS Base Router Configuration Standard

**Repository:** CCNA-Engineering-Residency
**Engineer:** LaToya Ellis
**Version:** 1.0

---

# Purpose

This document defines the standard baseline configuration applied to every Cisco router used throughout this residency. Establishing a consistent starting configuration reduces configuration errors, improves security, and mirrors common enterprise deployment practices.

---

# Base Configuration

```cisco
enable
configure terminal

! Hostname
hostname R-HQ-01

! Disable DNS lookup for mistyped commands
no ip domain-lookup

! Secure privileged EXEC mode
enable secret ChangeMe123!

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

! Local administrator account
username admin privilege 15 secret ChangeMe123!

! Domain name
ip domain-name lab.local

! Generate RSA keys for SSH
crypto key generate rsa modulus 2048

! Use SSH Version 2
ip ssh version 2

! Console configuration
line console 0
 logging synchronous
 exec-timeout 10 0
 login local
 exit

! VTY configuration
line vty 0 4
 login local
 transport input ssh
 exec-timeout 10 0
 exit

! Disable unused HTTP services
no ip http server
no ip http secure-server

end

copy running-config startup-config
```

---

# Configuration Breakdown

## Hostname

```cisco
hostname R-HQ-01
```

Assigns a unique, descriptive hostname that matches the repository naming convention.

---

## Disable DNS Lookup

```cisco
no ip domain-lookup
```

Prevents IOS from attempting DNS resolution when an invalid command is entered, avoiding unnecessary delays.

---

## Enable Secret

```cisco
enable secret ChangeMe123!
```

Protects privileged EXEC mode with an encrypted password. `enable secret` should be used instead of the older `enable password`.

---

## Password Encryption

```cisco
service password-encryption
```

Encrypts passwords stored in the running configuration to reduce casual exposure.

---

## Local User Account

```cisco
username admin privilege 15 secret ChangeMe123!
```

Creates a local administrative account used for console and SSH authentication.

---

## SSH Configuration

```cisco
ip domain-name lab.local
crypto key generate rsa modulus 2048
ip ssh version 2
```

Enables secure remote administration using SSH Version 2.

---

## Console Configuration

```cisco
line console 0
 logging synchronous
 exec-timeout 10 0
 login local
```

- `logging synchronous` prevents log messages from interrupting command entry.
- `exec-timeout` disconnects inactive sessions after 10 minutes.
- `login local` authenticates against the local user database.

---

## VTY Configuration

```cisco
line vty 0 4
 login local
 transport input ssh
 exec-timeout 10 0
```

Allows remote management using SSH only and disables Telnet access.

---

## Disable HTTP Services

```cisco
no ip http server
no ip http secure-server
```

Disables the embedded web management service when it is not required, reducing the attack surface.

---

# Interface Configuration Template

```cisco
interface GigabitEthernet0/0

 description Connection to SW-HQ-01 G0/1

 ip address 10.10.10.1 255.255.255.0

 no shutdown
```

Always include:

- Interface description
- IP address (if Layer 3)
- `no shutdown`

---

# Saving the Configuration

```cisco
copy running-config startup-config
```

Save the running configuration to NVRAM after verifying the deployment.

---

# Verification Commands

```cisco
show running-config

show startup-config

show ip interface brief

show interfaces

show version

show users

show ip ssh

show crypto key mypubkey rsa
```

---

# Security Best Practices

- Use unique hostnames.
- Replace default passwords immediately.
- Use `enable secret` instead of `enable password`.
- Use SSH instead of Telnet.
- Configure interface descriptions.
- Shut down unused interfaces.
- Save the configuration after successful validation.
- Document all configuration changes.

---

# Lab Customization

Update the following values for each deployment:

| Setting                | Example                 |
| ---------------------- | ----------------------- |
| Hostname               | R-BR1-01                |
| IP Address             | 10.20.20.1/24           |
| Domain Name            | branch.local            |
| Username               | admin                   |
| Interface Descriptions | Match connected devices |

---

# Baseline Validation Checklist

- [ ] Hostname configured
- [ ] DNS lookup disabled
- [ ] Enable secret configured
- [ ] Local administrator account created
- [ ] Password encryption enabled
- [ ] MOTD banner configured
- [ ] SSH Version 2 enabled
- [ ] RSA keys generated
- [ ] Console secured
- [ ] VTY secured
- [ ] HTTP services disabled
- [ ] Interface descriptions added
- [ ] Configuration saved
- [ ] Verification commands completed

---

# Related Documentation

- Naming Conventions
- Device Inventory
- Engineering Ticket
- Lab Report
- Verification Checklist

---

# Revision History

| Version | Date | Author       | Changes         |
| ------- | ---- | ------------ | --------------- |
| 1.0     |      | LaToya Ellis | Initial version |
# Cisco IOS Base Router Configuration Standard

**Repository:** CCNA-Engineering-Residency
**Engineer:** LaToya Ellis
**Version:** 1.0

---

# Purpose

This document defines the standard baseline configuration applied to every Cisco router used throughout this residency. Establishing a consistent starting configuration reduces configuration errors, improves security, and mirrors common enterprise deployment practices.

---

# Base Configuration

```cisco
enable
configure terminal

! Hostname
hostname R-HQ-01

! Disable DNS lookup for mistyped commands
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

! Local administrator account
username admin privilege 15 secret <SET_SECURE_PASSWORD>

! Domain name
ip domain-name lab.local

! Generate RSA keys for SSH
crypto key generate rsa modulus 2048

! Use SSH Version 2
ip ssh version 2

! Console configuration
line console 0
 logging synchronous
 exec-timeout 10 0
 login local
 exit

! VTY configuration
line vty 0 4
 login local
 transport input ssh
 exec-timeout 10 0
 exit

! Disable unused HTTP services
no ip http server
no ip http secure-server

end

copy running-config startup-config
```

---

# Configuration Breakdown

## Hostname

```cisco
hostname R-HQ-01
```

Assigns a unique, descriptive hostname that matches the repository naming convention.

---

## Disable DNS Lookup

```cisco
no ip domain-lookup
```

Prevents IOS from attempting DNS resolution when an invalid command is entered, avoiding unnecessary delays.

---

## Enable Secret

```cisco
enable secret ChangeMe123!
```

Protects privileged EXEC mode with an encrypted password. `enable secret` should be used instead of the older `enable password`.

---

## Password Encryption

```cisco
service password-encryption
```

Encrypts passwords stored in the running configuration to reduce casual exposure.

---

## Local User Account

```cisco
username admin privilege 15 secret ChangeMe123!
```

Creates a local administrative account used for console and SSH authentication.

---

## SSH Configuration

```cisco
ip domain-name lab.local
crypto key generate rsa modulus 2048
ip ssh version 2
```

Enables secure remote administration using SSH Version 2.

---

## Console Configuration

```cisco
line console 0
 logging synchronous
 exec-timeout 10 0
 login local
```

- `logging synchronous` prevents log messages from interrupting command entry.
- `exec-timeout` disconnects inactive sessions after 10 minutes.
- `login local` authenticates against the local user database.

---

## VTY Configuration

```cisco
line vty 0 4
 login local
 transport input ssh
 exec-timeout 10 0
```

Allows remote management using SSH only and disables Telnet access.

---

## Disable HTTP Services

```cisco
no ip http server
no ip http secure-server
```

Disables the embedded web management service when it is not required, reducing the attack surface.

---

# Interface Configuration Template

```cisco
interface GigabitEthernet0/0

 description Connection to SW-HQ-01 G0/1

 ip address 10.10.10.1 255.255.255.0

 no shutdown
```

Always include:

- Interface description
- IP address (if Layer 3)
- `no shutdown`

---

# Saving the Configuration

```cisco
copy running-config startup-config
```

Save the running configuration to NVRAM after verifying the deployment.

---

# Verification Commands

```cisco
show running-config

show startup-config

show ip interface brief

show interfaces

show version

show users

show ip ssh

show crypto key mypubkey rsa
```

---

# Security Best Practices

- Use unique hostnames.
- Replace default passwords immediately.
- Use `enable secret` instead of `enable password`.
- Use SSH instead of Telnet.
- Configure interface descriptions.
- Shut down unused interfaces.
- Save the configuration after successful validation.
- Document all configuration changes.

---

# Lab Customization

Update the following values for each deployment:

| Setting | Example |
|---------|---------|
| Hostname | R-BR1-01 |
| IP Address | 10.20.20.1/24 |
| Domain Name | branch.local |
| Username | admin |
| Interface Descriptions | Match connected devices |

---

# Baseline Validation Checklist

- [ ] Hostname configured
- [ ] DNS lookup disabled
- [ ] Enable secret configured
- [ ] Local administrator account created
- [ ] Password encryption enabled
- [ ] MOTD banner configured
- [ ] SSH Version 2 enabled
- [ ] RSA keys generated
- [ ] Console secured
- [ ] VTY secured
- [ ] HTTP services disabled
- [ ] Interface descriptions added
- [ ] Configuration saved
- [ ] Verification commands completed

---

# Related Documentation

- Naming Conventions
- Device Inventory
- Engineering Ticket
- Lab Report
- Verification Checklist

---

# Revision History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | | LaToya Ellis | Initial version |
