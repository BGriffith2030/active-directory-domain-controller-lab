# Project Overview

## Introduction

The Active Directory Domain Controller Lab is a virtualized environment designed to simulate a small enterprise Windows infrastructure. This project focuses on deploying a Windows Server 2022 Domain Controller, configuring Active Directory Domain Services (AD DS), setting up DNS, and onboarding a Windows 11 workstation into the domain.

The purpose of this lab is to build hands-on experience with identity management, system administration, networking fundamentals, and enterprise IT operations.

---

## Lab Goals

This project aims to:

- Deploy a fully functional Windows Server 2022 domain controller
- Configure Active Directory Domain Services (AD DS)
- Implement DNS for domain operations
- Create Organizational Units (OUs), users, and security groups
- Build and configure a Windows 11 domain workstation
- Demonstrate core identity and access management concepts
- Document each configuration step with screenshots and explanations

---

## Environment Summary

### Domain
griffith.local

### Systems

| System              | Role                                           |
| ------------------- | ---------------------------------------------- |
| Windows Server 2022 | Domain Controller, AD DS, DNS                  |
| Windows 11          | Domain Workstation / Client                    |

---

## Architecture Overview

The lab uses VirtualBox to host both the domain controller and the Windows 11 workstation. Networking is configured using NAT + Host-Only adapters to allow:

- Internet access for updates  
- Internal communication between DC01 and WIN11  
- DNS resolution inside the domain  

The domain controller manages authentication, identity, and directory services for the environment.

---

## Key Components

### Active Directory Domain Services (AD DS)
- Domain creation  
- Organizational Units  
- Security Groups  
- User Accounts  
- Domain authentication  

### DNS Configuration
- Forward lookup zones  
- Host records  
- Domain name resolution  

### Windows 11 Client
- Network configuration  
- Domain join  
- User login validation  

---

## Skills Practiced

- Windows Server installation and configuration  
- Domain controller promotion  
- DNS setup and troubleshooting  
- Identity and access management  
- Organizational Unit design  
- Workstation domain onboarding  
- Technical documentation  
- Virtualization and networking  

---

## Project Structure

active-directory-domain-controller-lab/
│
├── docs/
│   ├── Project-Overview.md
│   ├── Environment-Setup.md
│   ├── Active-Directory-Guide.md
│   ├── Networking-Guide.md
│   └── Windows-Client-Guide.md
│
├── diagrams/
├── screenshots/
├── scripts/
└── README.md


---

## Documentation Included

This project includes:

- Environment setup instructions  
- Active Directory configuration guide  
- Networking configuration guide  
- Windows client setup guide  
- Architecture diagrams  
- Screenshot gallery  
- Technical explanations  

---

## Conclusion

This lab provides a complete, hands-on demonstration of building a functional Windows domain environment from scratch. It showcases essential system administration skills, identity management concepts, and enterprise IT fundamentals — all documented and organized in a professional GitHub format.



