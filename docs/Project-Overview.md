# Project Overview

## Introduction

This project documents the design, deployment, and configuration of a Windows Server 2022 Active Directory Domain Controller within a virtualized lab environment using Oracle VirtualBox.

The primary objective of this lab was to gain practical experience deploying Microsoft's Active Directory Domain Services (AD DS) from the ground up while documenting each stage of the implementation. The environment was designed to simulate the foundational components of an enterprise Windows domain, including centralized identity management, DNS services, user administration, and organizational structure.

Rather than focusing only on installation, this project emphasizes planning, documentation, troubleshooting, and repeatable deployment practices commonly used by systems administrators and enterprise IT teams.

---

# Project Goals

The goals of this project were to:

- Build a Windows Server 2022 virtual machine using Oracle VirtualBox.
- Configure enterprise-style virtual networking.
- Assign static IPv4 addressing.
- Install and configure Active Directory Domain Services (AD DS).
- Promote the server to a Domain Controller.
- Create a new Active Directory forest named **griffith.local**.
- Configure DNS to support Active Directory.
- Design a logical Organizational Unit (OU) structure.
- Create domain user accounts.
- Create security groups for administration.
- Document every major deployment step with screenshots.
- Build a professional GitHub portfolio project suitable for demonstrating Windows Server administration skills.

---

# Project Scope

This repository focuses on the successful deployment and initial configuration of a Windows Server Active Directory environment.

Completed components include:

- Oracle VirtualBox installation
- Virtual machine creation
- Windows Server 2022 installation
- Virtual hardware configuration
- Network adapter configuration
- Static IP configuration
- Active Directory Domain Services installation
- Domain Controller promotion
- DNS configuration
- Organizational Unit creation
- User account management
- Security group management
- Technical documentation

The project intentionally concludes after the successful deployment of the Domain Controller. Client domain integration and advanced enterprise administration are planned as future enhancements.

---

# Lab Environment

## Host Platform

- Oracle VirtualBox

## Server Operating System

- Windows Server 2022

## Server Name

- DC01

## Domain Name

- griffith.local

## Network Configuration

- Host-Only Virtual Network

---

# Technologies Used

| Technology | Purpose |
|------------|---------|
| Windows Server 2022 | Domain Controller |
| Oracle VirtualBox | Virtualization |
| Active Directory Domain Services | Identity Management |
| DNS | Name Resolution |
| IPv4 | Network Configuration |
| Git | Version Control |
| GitHub | Documentation and Portfolio |

---

# Skills Demonstrated

This project demonstrates practical experience with:

- Windows Server administration
- Active Directory deployment
- DNS configuration
- IPv4 networking
- Virtual machine administration
- Organizational Unit management
- User account administration
- Security group management
- Technical troubleshooting
- Documentation best practices

---

# Deliverables

This repository contains:

- Complete project documentation
- Deployment walkthrough
- Configuration notes
- Network architecture diagrams
- Deployment screenshots
- Lessons learned
- Future enhancement roadmap

---

# Learning Outcomes

Upon completion of this project, the following competencies were demonstrated:

- Understanding of enterprise identity management fundamentals.
- Practical deployment of Active Directory Domain Services.
- Configuration of DNS services supporting Active Directory.
- Administration of Windows Server within a virtualized environment.
- Creation and organization of enterprise directory objects.
- Documentation of infrastructure deployments using GitHub.

---

# Future Development

Future iterations of this project will expand the environment by adding:

- Windows 11 Pro domain client
- Domain joining
- Group Policy Objects (GPOs)
- File sharing and NTFS permissions
- PowerShell automation
- Security auditing
- Event log monitoring
- Active Directory backup and recovery

These additions will transform the current deployment into a more complete enterprise Active Directory lab while maintaining this repository as the foundation of the overall project.





