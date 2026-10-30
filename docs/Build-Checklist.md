# Build Checklist: Domain Controller Deployment

The condensed, repeatable version of the deployment documented in this repository's README. Values shown are this lab's actual configuration. Checkboxes are ordered; each phase ends with a verification step, because a phase that is not verified is not finished.

**Lab values:** Hostname DC01 · Windows Server 2022 · Domain griffith.local · Static IPv4 192.168.56.101 · Hypervisor Oracle VirtualBox · Network Host-Only

## Phase 1 — Environment preparation

- [ ] Download the Windows Server 2022 installation ISO
- [ ] Install Oracle VirtualBox
- [ ] Create the project folder structure (docs, diagrams, screenshots, scripts)
- [ ] Take a screenshot of the prepared environment for the evidence set

## Phase 2 — Virtual machine deployment

- [ ] Create the DC01 virtual machine
- [ ] Assign virtual hardware (CPU, RAM) sized for a lab domain controller
- [ ] Create the virtual disk
- [ ] Configure the network adapter as Host-Only
- [ ] Screenshot the hardware and network settings

## Phase 3 — Windows Server installation

- [ ] Install Windows Server 2022 (Desktop Experience)
- [ ] Rename the server to DC01 and restart
- [ ] Set the static IPv4 address: 192.168.56.101, with DNS pointing at itself once DNS is installed
- [ ] Verify connectivity on the host-only network (ping a second lab machine or the host adapter)

## Phase 4 — Active Directory deployment

- [ ] Install the Active Directory Domain Services role
- [ ] Promote the server to a domain controller, creating the new forest griffith.local
- [ ] Confirm DNS was installed and integrated with the promotion
- [ ] Restart, then log on with a domain admin account
- [ ] Verify: `dcdiag` runs clean, DNS resolves the domain name, and the SRV records exist

## Phase 5 — Directory administration

- [ ] Create the Organizational Unit structure
- [ ] Create the domain user accounts
- [ ] Create the security groups and add members
- [ ] Verify: users and groups visible in Active Directory Users and Computers, and a test user can be managed (password reset, disable, enable)

## Phase 6 — Client preparation

- [ ] Create the Windows 11 virtual machine with host-only networking
- [ ] Record the edition requirement: domain join needs Windows 11 Pro or better; Windows 11 Home cannot join a domain (found during this lab's testing and documented in Troubleshooting)
- [ ] Point the client's DNS at 192.168.56.101 before any domain join attempt

## After the build

- [ ] Apply the settings in [Hardening.md](Hardening.md)
- [ ] Take a hypervisor snapshot of the known good domain controller
- [ ] Update the README evidence set with the final screenshots

## The rule this checklist teaches

Every phase separates doing from proving. Install, then verify. Promote, then `dcdiag`. Create, then test. That habit, more than any single setting, is what transfers from this lab to a production network.
