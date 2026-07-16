# Active Directory Deployment

# Overview

This document describes the deployment and initial configuration of Microsoft Active Directory Domain Services (AD DS) within the Active Directory Domain Controller Lab.

Active Directory is Microsoft's centralized identity and access management platform. It provides authentication, authorization, directory services, and centralized administration for Windows-based enterprise environments.

In this lab, Windows Server 2022 was promoted to a Domain Controller to create a new Active Directory forest and domain. Organizational Units (OUs), user accounts, and security groups were then created to simulate a basic enterprise directory structure.

---

# Project Objectives

The Active Directory deployment was designed to accomplish the following objectives:

- Install Active Directory Domain Services (AD DS)
- Promote Windows Server to a Domain Controller
- Create a new Active Directory forest
- Configure integrated DNS
- Create Organizational Units (OUs)
- Create domain users
- Create security groups
- Build a repeatable enterprise deployment

---

# Active Directory Domain Services (AD DS)

Active Directory Domain Services was installed using Windows Server Manager.

The AD DS role provides:

- Centralized authentication
- Centralized authorization
- Directory Services
- Group Policy support
- Domain management
- User and computer management

Installing AD DS prepares Windows Server to function as a Domain Controller.

---

# Domain Controller Promotion

After installing AD DS, the server was promoted to a Domain Controller.

During promotion the following tasks were completed:

- Created a new Active Directory forest
- Installed integrated DNS
- Configured the Global Catalog
- Configured SYSVOL
- Completed server promotion
- Rebooted the server

This process transforms Windows Server into the first Domain Controller within the environment.

---

# Active Directory Forest

Forest Name

```
griffith.local
```

The forest is the highest logical security boundary within Active Directory.

This lab uses a single forest and a single domain to simplify administration while demonstrating enterprise deployment concepts.

---

# Domain Structure

```
griffith.local
│
├── Domain Controllers
├── Users
├── Groups
└── Organizational Units
```

This structure provides centralized administration while allowing future expansion.

---

# Organizational Units (OUs)

Organizational Units were created to logically organize directory objects.

Benefits include:

- Administrative delegation
- Easier management
- Group Policy targeting
- Better organization
- Scalability

Using Organizational Units keeps the directory organized as the environment grows.

---

# User Accounts

Domain user accounts were created to simulate enterprise users.

Examples of administrative tasks include:

- Creating users
- Managing passwords
- Assigning users to Organizational Units
- Managing account properties

Centralized user management is one of the primary functions of Active Directory.

---

# Security Groups

Security groups were created to simplify permission management.

Benefits include:

- Role-based access control
- Simplified administration
- Easier permission assignment
- Centralized management

Rather than assigning permissions directly to users, enterprise environments typically assign permissions to security groups.

---

# DNS Integration

Active Directory depends heavily on DNS.

The Domain Controller was also configured as the DNS server.

DNS provides:

- Domain name resolution
- Service location
- Authentication support
- Domain Controller discovery

Without DNS, Active Directory clients cannot locate domain services.

---

# Administration Tools

The following Windows administrative tools were used during deployment:

- Server Manager
- Active Directory Users and Computers
- DNS Manager
- Windows Server Tools

These utilities provide centralized management of Active Directory infrastructure.

---

# Deployment Verification

After deployment, several verification tasks were completed.

Examples included:

- Confirming Domain Controller promotion
- Verifying Active Directory Users and Computers
- Confirming Organizational Units
- Verifying user accounts
- Verifying security groups
- Confirming DNS functionality

These verification steps ensured that the Active Directory deployment completed successfully.

---

# Best Practices

Several enterprise best practices were followed during deployment.

These include:

- Dedicated Domain Controller
- Static IP addressing
- Integrated DNS
- Organized Organizational Unit structure
- Security group management
- Centralized user administration
- Deployment documentation

These practices improve maintainability, scalability, and operational consistency.

---

# Lessons Learned

Deploying Active Directory reinforced several key enterprise concepts.

Most importantly:

- Active Directory relies on properly configured DNS.
- Static IP addresses are required for infrastructure servers.
- Organizational Units improve administration.
- Security groups simplify access management.
- Thorough documentation makes deployments repeatable.

Understanding these relationships is essential for Windows Server administration and enterprise IT operations.

---

# Summary

The successful deployment of Active Directory Domain Services established the foundation of the lab environment.

The completed deployment provides centralized identity management, integrated DNS services, user administration, and organizational structure while demonstrating the core responsibilities of a Windows Server Domain Controller.

This implementation also provides a foundation for future enhancements including Windows domain clients, Group Policy Objects (GPOs), PowerShell automation, and additional enterprise administration scenarios.
