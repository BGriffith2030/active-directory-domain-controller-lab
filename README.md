# Enterprise Active Directory Domain Controller Deployment

> **Windows Server 2022 • Active Directory Domain Services (AD DS) • DNS • Oracle VirtualBox • Windows Administration • Enterprise Documentation**

![Windows Server](https://img.shields.io/badge/Windows_Server-2022-0078D6?style=for-the-badge&logo=windows)
![Active Directory](https://img.shields.io/badge/Active_Directory-AD_DS-00A4EF?style=for-the-badge)
![Oracle VirtualBox](https://img.shields.io/badge/Oracle-VirtualBox-F80000?style=for-the-badge&logo=virtualbox)
![DNS](https://img.shields.io/badge/DNS-Configured-228B22?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

---

# Enterprise Windows Infrastructure Project

This project documents the design, deployment, and configuration of a **Windows Server 2022 Active Directory Domain Controller** within an isolated enterprise lab environment using **Oracle VirtualBox**.

The objective was to simulate the deployment of a foundational Windows domain by configuring Active Directory Domain Services (AD DS), integrated DNS, static networking, Organizational Units (OUs), user accounts, and security groups while documenting every phase of the implementation.

The project emphasizes practical Windows Server administration, enterprise networking fundamentals, infrastructure documentation, and repeatable deployment practices.

---

# Technical Skills Demonstrated

- Windows Server 2022 Administration
- Active Directory Domain Services (AD DS)
- DNS Configuration & Verification
- Oracle VirtualBox Administration
- Virtual Machine Deployment
- Static IPv4 Configuration
- Enterprise Networking Fundamentals
- Organizational Unit (OU) Design
- User & Group Administration
- Security Group Management
- Infrastructure Documentation
- Technical Troubleshooting
- Git & GitHub

---

# Technologies

| Category | Technology |
|-----------|------------|
| Operating System | Windows Server 2022 |
| Virtualization | Oracle VirtualBox |
| Directory Services | Active Directory Domain Services |
| Name Resolution | Microsoft DNS |
| Networking | IPv4, Static IP Addressing |
| Documentation | Markdown |
| Version Control | Git |
| Repository | GitHub |

---

# Project Objectives

The primary goals of this deployment were to:

- Deploy Windows Server 2022
- Configure Oracle VirtualBox
- Configure Host-Only Networking
- Assign Static IPv4 Addressing
- Install Active Directory Domain Services
- Promote the Server to a Domain Controller
- Create the **griffith.local** Active Directory Forest
- Configure Integrated DNS
- Create Organizational Units
- Create Domain User Accounts
- Create Security Groups
- Document the deployment from start to finish

---

# Lab Environment

## Domain Controller

| Configuration | Value |
|--------------|-------|
| Hostname | DC01 |
| Operating System | Windows Server 2022 |
| Domain | griffith.local |
| IPv4 Address | 192.168.56.101 |
| Virtualization Platform | Oracle VirtualBox |

---

# Deployment Workflow

The deployment followed the sequence below:

### Phase 1 — Environment Preparation

- Download Windows Server installation media
- Install Oracle VirtualBox
- Prepare project structure
- Configure virtualization environment

Reference Screenshots

- 01-Operating-System-ISOs.png
- 02-VirtualBox-Installed.png
- 03-VirtualBox-Storage-Location.png

---

### Phase 2 — Virtual Machine Deployment

- Create DC01 Virtual Machine
- Configure virtual hardware
- Configure storage
- Configure networking

Reference Screenshots

- 06-Create-DC01-VM.png
- 06-DC01-Hardware-Settings-1.png
- 07-DC01-Hardware-Settings-2.png
- 08-DC01-Virtual-Disk.png
- 09-DC01-Created.png
- 10-DC01-Network-Adapters.png

---

### Phase 3 — Windows Server Installation

- Install Windows Server 2022
- Rename server to DC01
- Configure Static IPv4 Address
- Verify network connectivity

Reference Screenshots

- 11-Windows-Server-Installing.png
- 12-DC01-Desktop.png
- 13-DC01-Renamed.png
- 14-DC01-Static-IP.png
- 15-DC01-Static-IP.png

---

### Phase 4 — Active Directory Deployment

- Install Active Directory Domain Services
- Promote Server to Domain Controller
- Configure DNS
- Create Active Directory Forest

Reference Screenshots

- 16-ADDS-Role-Installed.png
- 17-Domain-Controller-Created.png
- 18-Active-Directory-Domain.png

---

### Phase 5 — Directory Administration

- Create Organizational Units
- Create User Accounts
- Create Security Groups

Reference Screenshots

- 19-Organizational-Units.png
- 20-Security-Groups.png
- 21-User-Accounts.png

---

### Phase 6 — Windows Client Preparation

A Windows 11 virtual machine was prepared as the foundation for future client integration. During testing it was determined that **Windows 11 Home** does not support joining an Active Directory domain. This limitation has been documented, and future enhancements include deploying a Windows 11 Pro client to complete domain integration.

Reference Screenshots

- 22-Windows11-VM-Creation.png
- 23-WIN11-Hardware-Settings.png
- 24-WIN11-Network-Settings.png
- 25-WIN11-Desktop.png

---

# Repository Structure

```
active-directory-domain-controller-lab
│
├── docs
│   ├── Project-Overview.md
│   ├── Environment-Setup.md
│   ├── Architecture.md
│   ├── Networking.md
│   ├── Active-Directory.md
│   ├── DNS.md
│   ├── User-Management.md
│   ├── Troubleshooting.md
│   ├── Lessons-Learned.md
│   └── Future-Enhancements.md
│
├── diagrams
│
├── screenshots
│
├── scripts
│
├── LICENSE
│
└── README.md
```

---

# Documentation

Complete documentation is available within the **docs** directory.

- [Project Overview](docs/Project-Overview.md)
- [Environment Setup](docs/Environment-Setup.md)
- [Architecture](docs/Architecture.md)
- [Networking](docs/Networking.md)
- [Active Directory](docs/Active-Directory.md)
- [DNS](docs/DNS.md)
- [User Management](docs/User-Management.md)
- [Troubleshooting](docs/Troubleshooting.md)
- [Lessons Learned](docs/Lessons-Learned.md)
- [Future Enhancements](docs/Future-Enhancements.md)

---

# Project Outcomes

Upon completion of this deployment, the following capabilities were demonstrated:

- Windows Server installation and administration
- Active Directory Domain Services deployment
- DNS implementation and verification
- Static network configuration
- Enterprise identity management
- Organizational Unit design
- User account administration
- Security group management
- Infrastructure troubleshooting
- Technical documentation using GitHub

---

# Lessons Learned

Key concepts reinforced during this project include:

- Active Directory depends heavily on DNS.
- Infrastructure servers should use static IP addressing.
- Enterprise environments benefit from organized OU structures.
- Security groups simplify permission management.
- Thorough documentation improves repeatability and maintainability.
- Systematic troubleshooting is more effective than trial-and-error.

---

# Future Enhancements

Planned future phases include:

- Windows 11 Pro Domain Client
- Domain Join
- Group Policy Objects (GPOs)
- File Server Deployment
- NTFS Permissions
- PowerShell Automation
- Security Auditing
- Windows Event Logging
- Active Directory Backup & Recovery
- Additional Domain Services

---

# About the Author

**Brandon Griffith**

Cybersecurity Graduate Student | Windows Systems Administration | Active Directory | Networking | Virtualization

This repository is part of my professional portfolio and demonstrates hands-on experience with Windows infrastructure deployment, enterprise identity management, virtualization, and technical documentation.

GitHub Portfolio:

https://github.com/BGriffith2030

---

# License

This project is licensed under the MIT License.

---

**Status:** ✅ Completed

This repository will continue to evolve as additional enterprise Windows infrastructure components are implemented and documented.

