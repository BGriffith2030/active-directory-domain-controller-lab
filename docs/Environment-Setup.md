# Environment Setup Guide

## Introduction

This guide explains how to set up the virtual environment used in the Active Directory Domain Controller Lab. You will install VirtualBox, prepare ISO files, create the Windows Server 2022 domain controller (DC01), and build the Windows 11 workstation (WIN11). Completing these steps ensures a clean, consistent, and functional lab environment.

---

## 1. Project Folder Structure

Your repository should contain the following folders:

diagrams/
docs/
screenshots/
scripts/
LICENSE
README.md


Inside **docs**, you will place all documentation files, including this one.

---

## 2. Install VirtualBox

Download and install VirtualBox:

https://www.virtualbox.org/wiki/Downloads

After installation:

- Launch VirtualBox  
- Confirm it opens without errors  
- Verify the default VM storage location  

---

## 3. Prepare ISO Files

Download the required operating system ISO files:

### Windows Server 2022 ISO
- Microsoft Evaluation Center  
- Save as: `Windows_Server_2022.iso`

### Windows 11 ISO
- Microsoft Software Download  
- Save as: `Windows_11.iso`

Place both ISO files inside a folder you create:

isos/


This keeps your operating system images organized.

---

## 4. Create and Install DC01 (Domain Controller)

### VM Configuration

- **Name:** DC01  
- **Type:** Microsoft Windows  
- **Version:** Windows Server 2022 (64‑bit)  
- **CPU:** 2 cores  
- **RAM:** 4096 MB  
- **Storage:** 50 GB  
- **Network:**  
  - Adapter 1: NAT  
  - Adapter 2: Host‑Only  

### Attach ISO

VirtualBox → DC01 → Settings → Storage → Add ISO  
Select: `Windows_Server_2022.iso`

### Install Windows Server 2022

- Boot the VM  
- Choose “Windows Server 2022 Standard (Desktop Experience)”  
- Create Administrator password  
- Log in  
- Install Windows updates  

### Rename the Server

Open PowerShell:

Rename-Computer -NewName "DC01" -Restart


### Configure Static IP

Set the following IPv4 settings:

IP Address: 192.168.10.10
Subnet Mask: 255.255.255.0
Default Gateway: 192.168.10.1
DNS Server: 192.168.10.10


This ensures the domain controller handles DNS internally.

---

## 5. Install Active Directory Domain Services (AD DS)

Open **Server Manager**:

- Add Roles and Features  
- Select **Active Directory Domain Services**  
- Complete installation  

After installation:

- Click **Promote this server to a domain controller**  
- Choose **Add a new forest**  
- Enter domain:

griffith.local


- Create DSRM password  
- Accept default paths  
- Install and reboot  

DC01 is now your domain controller.

---

## 6. Create Windows 11 Client (WIN11)

### VM Configuration

- **Name:** WIN11  
- **Type:** Microsoft Windows  
- **Version:** Windows 11 (64‑bit)  
- **CPU:** 2 cores  
- **RAM:** 4096 MB  
- **Storage:** 64 GB  
- **Network:**  
  - Adapter 1: NAT  
  - Adapter 2: Host‑Only  

### Attach ISO

VirtualBox → WIN11 → Settings → Storage → Add ISO  
Select: `Windows_11.iso`

### Install Windows 11

- Choose region and keyboard  
- Create a local account  
- Log in  
- Install Windows updates  

---

## 7. Configure Windows 11 Networking

Set DNS to the domain controller:

DNS Server: 192.168.10.10


Verify connectivity:

ping dc01.griffith.local


If the ping succeeds, networking is correct.

---

## 8. Join Windows 11 to the Domain

Open System Settings:

- Rename this PC (Advanced)  
- Change → Domain: `griffith.local`  
- Enter domain credentials  
- Restart the workstation  

Log in using:

griffith\username


---

## Conclusion

Your environment is now fully set up:

- VirtualBox installed  
- Windows Server 2022 domain controller configured  
- Windows 11 workstation deployed  
- Networking configured  
- Domain join successful  

You are ready to continue with Active Directory configuration and user management.


