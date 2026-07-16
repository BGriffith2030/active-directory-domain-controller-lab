# Troubleshooting

# Overview

This document summarizes the issues encountered during the deployment of the Active Directory Domain Controller Lab and the steps taken to identify and resolve them.

Troubleshooting was an important part of this project. Rather than simply following installation steps, the deployment required investigating networking, virtualization, and Windows configuration issues. Each issue provided an opportunity to better understand how Windows Server, Active Directory, DNS, and Oracle VirtualBox interact.

---

# Troubleshooting Methodology

When problems were encountered, a consistent process was followed:

1. Identify the problem.
2. Verify system configuration.
3. Test network connectivity.
4. Review Windows Server settings.
5. Validate DNS functionality.
6. Apply corrective actions.
7. Verify that the issue was resolved.
8. Document the solution.

This structured approach mirrors the troubleshooting process commonly used by enterprise IT teams.

---

# Issue 1 – Static IP Configuration

## Problem

The Domain Controller required a static IP address before Active Directory could be reliably deployed.

## Resolution

Configured a static IPv4 address:

```
Hostname: DC01

IPv4 Address:
192.168.56.101

Subnet Mask:
255.255.255.0
```

This ensured the Domain Controller maintained a consistent network identity.

---

# Issue 2 – Virtual Network Configuration

## Problem

Communication between virtual machines required proper VirtualBox network configuration.

## Resolution

Configured a Host-Only Network Adapter within Oracle VirtualBox to create an isolated lab environment.

Verification included:

- Network adapter review
- IP configuration verification
- Connectivity testing

---

# Issue 3 – Network Connectivity

## Problem

Network communication needed to be verified before continuing with Active Directory deployment.

## Resolution

Connectivity testing was performed using:

```cmd
ping
```

Successful responses confirmed communication between systems.

---

# Issue 4 – DNS Verification

## Problem

Active Directory relies heavily on DNS.

Incorrect DNS configuration can prevent clients from locating Domain Controllers.

## Resolution

DNS functionality was verified using:

```cmd
nslookup
```

Testing confirmed:

- DNS server responsiveness
- Domain name resolution
- Active Directory service discovery

---

# Issue 5 – Active Directory Deployment

## Problem

After installing Active Directory Domain Services, the server required promotion to a Domain Controller.

## Resolution

The server was successfully promoted by:

- Creating a new forest
- Creating the **griffith.local** domain
- Installing integrated DNS
- Restarting the server

Verification confirmed that Active Directory services were operational.

---

# Issue 6 – Windows 11 Client Limitation

## Problem

A Windows 11 Home virtual machine was prepared for future client integration.

During testing, it was determined that Windows 11 Home does not support joining an Active Directory domain.

## Resolution

The limitation was documented, and future project enhancements include deploying a Windows 11 Pro client to complete domain integration.

This experience reinforced the importance of verifying operating system editions before deployment.

---

# Commands Used

Several built-in Windows networking commands were used throughout deployment.

### View IP Configuration

```cmd
ipconfig
```

---

### Test Connectivity

```cmd
ping
```

---

### Verify DNS

```cmd
nslookup
```

These tools are fundamental for diagnosing Windows networking and Active Directory issues.

---

# Lessons from Troubleshooting

The deployment reinforced several important concepts:

- Active Directory depends on DNS.
- Infrastructure servers require static IP addresses.
- Networking should always be verified before deploying services.
- Small configuration errors can produce significant issues.
- Systematic troubleshooting is more effective than trial and error.
- Thorough documentation improves repeatability and future maintenance.

---

# Summary

Troubleshooting was an essential part of this deployment and contributed significantly to the overall learning experience.

By diagnosing networking issues, validating DNS functionality, configuring Active Directory, and documenting Windows edition limitations, this project strengthened practical troubleshooting skills that are directly applicable to Windows Server administration and enterprise IT environments.

The experience also established a solid foundation for future enhancements, including Windows 11 Pro client deployment, Group Policy implementation, and additional Active Directory administration scenarios.
