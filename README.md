# Active Directory Domain Controller Deployment Lab

![Windows Server](https://img.shields.io/badge/Windows%20Server-2022-blue)
![VirtualBox](https://img.shields.io/badge/Oracle-VirtualBox-orange)
![Active Directory](https://img.shields.io/badge/Active%20Directory-AD%20DS-green)
![DNS](https://img.shields.io/badge/DNS-Configured-success)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)

---

# Overview

This project documents the deployment and configuration of a Windows Server 2022 Active Directory Domain Controller in a virtual lab environment using Oracle VirtualBox.

The objective was to design and deploy a functional Active Directory environment from the ground up while documenting each phase of the deployment process. The project includes virtual machine provisioning, Windows Server installation, network configuration, Active Directory Domain Services (AD DS) deployment, DNS configuration, Organizational Unit (OU) design, user management, and security group creation.

This repository is intended to demonstrate practical Windows Server administration skills, Active Directory fundamentals, enterprise networking concepts, and technical documentation practices.

---

# Project Objectives

- Deploy Windows Server 2022 in Oracle VirtualBox
- Configure virtual networking
- Assign static IPv4 addressing
- Install Active Directory Domain Services (AD DS)
- Promote the server to a Domain Controller
- Create a new Active Directory forest
- Configure DNS
- Design Organizational Units (OUs)
- Create domain users
- Create security groups
- Document the complete deployment process
- Build a professional GitHub portfolio project

---

# Skills Demonstrated

- Windows Server Administration
- Active Directory Domain Services
- DNS Administration
- Virtual Machine Deployment
- Oracle VirtualBox
- IPv4 Networking
- Static IP Configuration
- Organizational Unit Design
- User Administration
- Security Group Management
- Enterprise Documentation
- Technical Troubleshooting
- Git & GitHub

---

# Technologies Used

| Technology | Purpose |
|------------|---------|
| Windows Server 2022 | Domain Controller |
| Oracle VirtualBox | Virtualization Platform |
| Active Directory Domain Services | Identity Management |
| DNS | Name Resolution |
| IPv4 | Network Configuration |
| Git | Version Control |
| GitHub | Project Documentation |

---

# Lab Environment

## Host Machine

- Oracle VirtualBox
- Windows Host Operating System

## Domain Controller

**Hostname**

DC01

**Operating System**

Windows Server 2022

**Domain**

griffith.local

**Host-Only Network**

192.168.56.101

---

# Project Walkthrough

The deployment followed the following phases:

## Phase 1

- Download installation media
- Install Oracle VirtualBox
- Create project structure
- Prepare deployment environment

---

## Phase 2

- Create Windows Server virtual machine
- Configure VM hardware
- Configure storage
- Configure networking

---

## Phase 3

- Install Windows Server 2022
- Rename server to DC01
- Configure static IPv4 addressing
- Verify connectivity

---

## Phase 4

- Install Active Directory Domain Services
- Create Active Directory forest
- Configure DNS
- Promote server to Domain Controller

---

## Phase 5

- Create Organizational Units
- Create user accounts
- Create security groups
- Configure basic Active Directory structure

---

# Repository Structure

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

# Documentation

Detailed project documentation can be found inside the **docs** folder.

- Project Overview
- Environment Setup
- Architecture
- Networking
- Active Directory
- DNS
- User Management
- Troubleshooting
- Lessons Learned
- Future Enhancements

---

# Screenshots

The deployment is documented with screenshots covering every major stage of the project.

Included screenshots document:

- Environment preparation
- Virtual machine creation
- Windows Server installation
- Network configuration
- Static IP assignment
- Active Directory deployment
- Organizational Units
- User creation
- Security groups
- DNS configuration

All screenshots are located in the **screenshots** directory.

---

# Lessons Learned

Throughout this project I gained hands-on experience with:

- Deploying Windows Server in a virtual environment
- Configuring enterprise networking
- Installing Active Directory Domain Services
- Understanding the relationship between Active Directory and DNS
- Managing users and security groups
- Building repeatable deployment documentation
- Troubleshooting networking and virtualization issues

---

# Future Enhancements

This project will continue to evolve with additional enterprise features including:

- Windows 11 Pro Domain Client
- Domain Join
- Group Policy Objects (GPOs)
- File Shares
- NTFS Permissions
- Roaming Profiles
- PowerShell Automation
- Windows Event Logging
- Security Auditing
- Active Directory Backup & Recovery

---

# Key Takeaways

This project demonstrates the complete deployment of a Windows Server 2022 Active Directory Domain Controller within a virtual lab environment. It provides practical experience with enterprise identity management, DNS, networking, virtualization, and systems administration while emphasizing technical documentation and repeatable deployment practices.

---

## Author

**Brandon Griffith**

Cybersecurity Graduate Student • Systems Administration • Active Directory • Windows Server • Networking • Virtualization

GitHub Portfolio:
https://github.com/BGriffith2030

---

**Project Status:** Complete (Domain Controller Deployment)

Future updates will expand this repository with enterprise client management, Group Policy, and additional Active Directory administration features.

