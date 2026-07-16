# Environment Setup

# Overview

This document describes the hardware, software, virtualization platform, networking, and project structure used to build the Active Directory Domain Controller lab environment.

The objective of this environment was to create a repeatable Windows Server 2022 deployment that closely resembles the foundation of an enterprise Active Directory infrastructure while remaining suitable for a personal cybersecurity home lab.

---

# Host Environment

The lab was deployed on a Windows-based host computer using Oracle VirtualBox as the virtualization platform.

The host system provides the compute resources required to run Windows Server 2022 and supporting virtual machines while allowing the lab environment to remain isolated from the production network.

---

# Virtualization Platform

**Oracle VirtualBox**

Oracle VirtualBox was selected because it is a free enterprise-grade hypervisor capable of supporting Windows Server environments, custom virtual networking, snapshots, and multiple virtual machines.

VirtualBox was used to:

- Create the Domain Controller virtual machine
- Allocate virtual hardware
- Configure storage
- Configure networking
- Manage virtual machine lifecycle

---

# Virtual Machine Configuration

## Virtual Machine Name

```
DC01
```

---

## Guest Operating System

```
Windows Server 2022
```

---

## Virtual Hardware

The virtual machine was configured with hardware resources appropriate for a small Active Directory deployment.

Example configuration:

- 2 Virtual CPUs
- 4–8 GB RAM
- Virtual Hard Disk
- EFI Boot Enabled
- Virtual Optical Drive for Windows Server installation media

---

# Storage Configuration

A dedicated virtual hard disk was created for the Windows Server operating system.

Installation media was attached through the VirtualBox virtual optical drive using the official Windows Server 2022 ISO image.

---

# Network Configuration

The lab uses Oracle VirtualBox virtual networking.

The Domain Controller was configured with a Host-Only Adapter to allow communication between virtual machines while keeping the environment isolated from the physical production network.

---

## Static IP Configuration

Domain Controller

```
Hostname:
DC01

IPv4:
192.168.56.101

Subnet Mask:
255.255.255.0
```

Static addressing ensures reliable DNS resolution and allows Active Directory services to function correctly.

---

# Active Directory Environment

Domain Name

```
griffith.local
```

Server Role

```
Domain Controller
```

Installed Services

- Active Directory Domain Services
- DNS Server

---

# Project Directory Structure

The GitHub repository is organized to separate documentation, screenshots, diagrams, and scripts.

```
active-directory-domain-controller-lab
│
├── docs
├── diagrams
├── screenshots
├── scripts
├── LICENSE
└── README.md
```

---

# Deployment Workflow

The environment was deployed using the following workflow:

1. Download Windows Server installation media.
2. Install Oracle VirtualBox.
3. Create the DC01 virtual machine.
4. Configure virtual hardware.
5. Install Windows Server 2022.
6. Configure static networking.
7. Install Active Directory Domain Services.
8. Promote the server to a Domain Controller.
9. Configure DNS.
10. Create Organizational Units, users, and security groups.
11. Document each deployment phase.

---

# Design Considerations

Several design decisions were made during deployment:

- Static IPv4 addressing for server reliability
- Host-Only networking for lab isolation
- Separate documentation for each deployment phase
- Screenshot capture throughout implementation
- GitHub used for version-controlled documentation

---

# Outcome

The environment provides a functional Windows Server 2022 Active Directory Domain Controller suitable for practicing:

- Windows Server administration
- Active Directory management
- DNS administration
- Virtual networking
- User and group administration
- Enterprise documentation
- Infrastructure troubleshooting

This environment serves as the foundation for future enhancements, including Windows client integration, Group Policy deployment, PowerShell automation, and additional enterprise administration scenarios.

