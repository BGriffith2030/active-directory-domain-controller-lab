# Lab Architecture

# Overview

This document describes the overall architecture of the Active Directory Domain Controller Lab.

The environment was designed to simulate the foundational components of a small enterprise Windows infrastructure using Oracle VirtualBox. The lab focuses on virtualization, Windows Server administration, Active Directory Domain Services (AD DS), DNS, and enterprise network design while maintaining a safe, isolated environment.

---

# Architecture Goals

The primary design objectives were:

- Deploy a Windows Server 2022 Domain Controller.
- Isolate the lab from the production network.
- Configure reliable name resolution using DNS.
- Simulate enterprise identity management.
- Create a repeatable deployment suitable for learning and documentation.
- Build a scalable foundation for future Active Directory expansion.

---

# High-Level Architecture

```
                  Host Computer
                        │
         Oracle VirtualBox Hypervisor
                        │
             Host-Only Virtual Network
                        │
               192.168.56.0/24
                        │
        ┌───────────────────────────┐
        │                           │
        │          DC01             │
        │ Windows Server 2022       │
        │ Active Directory          │
        │ DNS Server                │
        │ 192.168.56.101            │
        └───────────────────────────┘
```

---

# Infrastructure Components

## Hypervisor

Oracle VirtualBox

Responsibilities:

- Virtual machine management
- Virtual networking
- Virtual storage
- Hardware abstraction

---

## Domain Controller

Hostname

```
DC01
```

Operating System

```
Windows Server 2022
```

Responsibilities

- Active Directory Domain Services
- DNS
- Authentication
- Directory Services
- User Administration
- Security Groups

---

# Network Design

The environment uses a Host-Only Network.

Advantages include:

- Isolated from production systems
- Safe for experimentation
- Predictable addressing
- Reliable communication between virtual machines
- Simplified troubleshooting

---

## Addressing Scheme

| Device | IP Address | Purpose |
|---------|------------|---------|
| DC01 | 192.168.56.101 | Domain Controller |

Subnet

```
255.255.255.0
```

---

# Active Directory Design

Forest

```
griffith.local
```

The environment uses a single forest and a single domain to simplify administration while demonstrating the core concepts of enterprise identity management.

---

# Directory Structure

```
griffith.local
│
├── Domain Controllers
├── Users
├── Security Groups
└── Organizational Units
```

This structure provides logical separation between administrative components and user objects.

---

# DNS Architecture

The Domain Controller also functions as the DNS Server.

Responsibilities include:

- Name resolution
- Active Directory service location
- Domain authentication support

DNS is tightly integrated with Active Directory and is required for domain functionality.

---

# Security Model

Although this lab focuses primarily on deployment rather than hardening, several best practices were incorporated.

These include:

- Static server addressing
- Dedicated Domain Controller
- Isolated virtual networking
- Centralized authentication
- Organized directory structure

Additional security controls are planned for future enhancements.

---

# Design Decisions

The following architectural decisions were made during deployment:

- Oracle VirtualBox selected as the hypervisor.
- Windows Server 2022 selected for enterprise compatibility.
- Host-Only networking used to isolate the environment.
- Single Domain Controller deployment for simplicity.
- DNS hosted on the Domain Controller.
- Static IP configuration for infrastructure reliability.
- GitHub used for version-controlled documentation.

---

# Scalability

The architecture was intentionally designed to support future expansion.

Planned additions include:

- Windows 11 Pro domain client
- Additional member servers
- Group Policy Objects (GPOs)
- File server
- PowerShell automation
- Security auditing
- Event log monitoring
- Backup and recovery testing

---

# Summary

This architecture provides a realistic foundation for learning enterprise Windows administration and Active Directory concepts while remaining lightweight enough to run on a personal computer.

The modular design also allows the environment to grow into a larger cybersecurity and systems administration home lab over time.
