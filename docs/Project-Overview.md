# Active Directory Domain Controller Lab

## Project Overview

This project demonstrates the deployment and configuration of a Windows Server–based Active Directory Domain Controller inside a virtualized lab environment. The goal is to replicate real‑world system administration tasks including domain creation, identity management, DNS configuration, workstation onboarding, and foundational enterprise IT operations.

This lab simulates a small business network using:

- Windows Server 2022 (Domain Controller)
- Windows 11 (Domain‑joined workstation)
- VirtualBox virtualization platform

The project includes full documentation, screenshots, diagrams, and a structured walkthrough of each configuration step.

---

## Project Objectives

- Build a functional Windows Server 2022 domain controller  
- Configure Active Directory Domain Services (AD DS)  
- Set up DNS for domain operations  
- Create Organizational Units (OUs), users, and security groups  
- Deploy and configure a Windows 11 domain workstation  
- Demonstrate core identity and access management concepts  
- Document each step with screenshots and technical explanations  
- Organize the project using a professional GitHub structure  

---

## Lab Environment

### Domain
griffith.local

### Systems

| System              | Purpose                                       |
| ------------------- | --------------------------------------------- |
| Windows Server 2022 | Domain Controller, AD DS, DNS                 |
| Windows 11          | Domain workstation/client                     |

---

## Technologies Used

### Operating Systems
- Windows Server 2022  
- Windows 11  

### Identity & Access Management
- Active Directory Domain Services  
- Organizational Units  
- Security Groups  
- User Accounts  
- Group Policy Objects (GPO)

### Administration Tools
- Server Manager  
- Active Directory Users and Computers  
- DNS Manager  
- PowerShell  
- VirtualBox  

---

## Skills Demonstrated

### System Administration
- Windows Server deployment  
- Domain controller configuration  
- DNS setup and verification  
- User and group management  
- Organizational Unit design  
- Workstation domain join  

### Networking
- Static IP configuration  
- DNS resolution  
- Host‑only and NAT networking  
- Client/server communication  

### Documentation
- Technical documentation  
- Screenshot‑based walkthroughs  
- Project organization using GitHub  

---

## Project Walkthrough

This project is organized into clear phases:

### Phase 1 — Environment Setup
- Install VirtualBox  
- Create project folders  
- Prepare Windows Server ISO  
- Build the DC01 virtual machine  

### Phase 2 — Domain Controller Configuration
- Install Windows Server  
- Rename server  
- Configure static IP  
- Install AD DS  
- Promote server to Domain Controller  
- Verify domain creation  

### Phase 3 — Active Directory Structure
- Create Organizational Units  
- Create Security Groups  
- Create User Accounts  

### Phase 4 — Windows 11 Client
- Build Windows 11 VM  
- Configure networking  
- Join workstation to the domain  

### Phase 5 — Final Verification
- Confirm domain membership  
- Validate user login  
- Review AD structure  

---

## Screenshot Gallery

### 🧱 Lab Setup
![Lab Setup](screenshots/01-Lab-Setup/01-Operating-System-ISOs.png)
![VirtualBox Installed](screenshots/01-Lab-Setup/02-VirtualBox-Installed.png)
![VirtualBox Storage](screenshots/01-Lab-Setup/03-VirtualBox-Storage-Location.png)
![Project Folders](screenshots/01-Lab-Setup/04-Project-Folders.png)
![Create DC01 VM](screenshots/01-Lab-Setup/05-Create-DC01-VM.png)
![DC01 Hardware Settings 1](screenshots/01-Lab-Setup/06-DC01-Hardware-Settings-1.png)
![DC01 Hardware Settings 2](screenshots/01-Lab-Setup/07-DC01-Hardware-Settings-2.png)
![DC01 Virtual Disk](screenshots/01-Lab-Setup/08-DC01-Virtual-Disk.png)

### 🏰 Active Directory
![Windows Server Installing](screenshots/02-Active-Directory/01-Windows-Server-Installing.png)
![DC01 Desktop](screenshots/02-Active-Directory/02-DC01-Desktop.png)
![DC01 Renamed](screenshots/02-Active-Directory/03-DC01-Renamed.png)
![ADDS Role Installed](screenshots/02-Active-Directory/04-ADDS-Role-Installed.png)
![Domain Controller Created](screenshots/02-Active-Directory/05-Domain-Controller-Created.png)
![Active Directory Domain](screenshots/02-Active-Directory/06-Active-Directory-Domain.png)

### 🌐 Network Configuration
![Network Adapters](screenshots/03-Network-Configuration/01-DC01-Network-Adapters.png)
![Static IP](screenshots/03-Network-Configuration/02-DC01-Static-IP.png)
![Static IP 2](screenshots/03-Network-Configuration/03-DC01-Static-IP-2.png)
![WIN11 Network Settings](screenshots/03-Network-Configuration/04-WIN11-Network-Settings.png)

### 💻 Windows Client
![Windows 11 VM Creation](screenshots/04-Windows-Client/01-Windows11-VM-Creation.png)
![WIN11 Hardware Settings](screenshots/04-Windows-Client/02-WIN11-Hardware-Settings.png)
![WIN11 Desktop](screenshots/04-Windows-Client/03-WIN11-Desktop.png)

### 🧩 Final
![Organizational Units](screenshots/05-Final/01-Organizational-Units.png)
![Security Groups](screenshots/05-Final/02-Security-Groups.png)
![User Accounts](screenshots/05-Final/03-User-Accounts.png)

---

## Project Documentation

This repository includes:

- Environment Setup Guide  
- Active Directory Configuration Guide  
- Networking Guide  
- Windows Client Guide  
- Diagrams  
- Screenshots and evidence  

All documentation is located in the `docs/` folder.

---

## Future Improvements

- Add Group Policy configuration  
- Add login scripts  
- Add roaming profiles  
- Add DHCP server  
- Add additional Windows clients  
- Add monitoring/logging tools  

---

## Project Status

✔️ Completed Core Deployment  
🚧 Additional Enhancements Planned  

---

## Author

**Brandon Griffith**  
Cybersecurity Student | IT Professional  
Focus Areas: System Administration, Cybersecurity, Identity Management



