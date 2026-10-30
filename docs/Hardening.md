# Hardening Guide: DC01 and the griffith.local Domain

This document is the security hardening layer for the domain built in this repository (DC01, Windows Server 2022, griffith.local, 192.168.56.101). The main README covers deployment; this guide covers what gets tightened after deployment, why, and how each setting is verified. Settings are applied through Group Policy so they are documented, repeatable, and enforced rather than set by hand and forgotten.

## 1. Account and password policy (Default Domain Policy)

| Setting | Value | Why |
| --- | --- | --- |
| Minimum password length | 14 characters | Length beats complexity tricks; 14 pushes cracking cost up sharply. |
| Password complexity | Enabled | Baseline hygiene on top of length. |
| Maximum password age | 90 days in the lab (modern guidance: change on suspicion, not on a calendar) | The lab practices the classic policy; the note matters more than the number. |
| Account lockout threshold | 5 invalid attempts | The same threshold the Windows Event Investigation Lab analyzer uses to call a burst brute force. |
| Lockout duration / reset | 15 minutes | Slows guessing without locking users out all day. |

## 2. Audit policy: turn on the events the SOC actually reads

Advanced Audit Policy on the domain controller and member machines:

- **Logon/Logoff:** Audit Logon (success and failure), Audit Logoff, Audit Special Logon. These produce Event IDs 4624, 4625, and 4672.
- **Account Management:** user account and group changes (4720 and friends).
- **Policy Change and System:** service installation auditing so Event 7045 is captured with context.

This is the supply side of the [Windows Event Investigation Lab](https://github.com/BGriffith2030/windows-event-investigation-lab): that lab's analyzer hunts 4625, 4624, 4672, 7045, and 4720, and none of those events exist to hunt unless this auditing is on. Hardening and detection are the same decision seen from two sides.

## 3. Services and protocols to remove or restrict

| Item | Action | Reason |
| --- | --- | --- |
| SMBv1 | Disable everywhere (feature removal on the server, GPO for members) | EternalBlue (CVE-2017-0144). See the [Vulnerability Management Lab](https://github.com/BGriffith2030/vulnerability-management-report-lab). |
| Print Spooler on DC01 | Disable the service | A domain controller does not print. PrintNightmare (CVE-2021-34527) made an unnecessary service into a domain level risk. |
| LLMNR and NetBIOS over TCP/IP | Disable via GPO | Stops a whole class of credential relay and poisoning attacks on flat networks. |
| RDP on DC01 | Restricted to the admin workstation by firewall rule and group membership; off entirely when not needed | The [Network Discovery Lab](https://github.com/BGriffith2030/network-discovery-security-assessment-lab) flagged RDP on the domain controller as its top contextual finding. |

## 4. Administrative hygiene

- Daily work happens in a standard user account; the domain admin account is used only at DC01, only for administration. (The investigation lab's scenario is what happens when a privileged account is also a daily driver.)
- Domain Admins membership is reviewed as part of every lab session; in a one person lab it should contain exactly one account.
- The built-in Administrator account is renamed and given a long unique password stored offline.

## 5. Verification

Hardening that is not verified is a rumor. After applying this guide:

1. `gpresult /h report.html` on DC01 confirms the policies actually applied.
2. `Get-SmbServerConfiguration` shows EnableSMB1Protocol = False.
3. A test burst of five bad passwords against a lab account produces five 4625 events and a lockout, visible in Event Viewer, which closes the loop with the investigation lab.
4. A fresh Nmap service scan (the network lab's methodology) shows 3389 no longer reachable from a non-admin host.

## Scope note

This is a lab domain on a host-only network, and the guide is written for it. In production the same settings ride on change control, testing against line of business applications, and a rollback plan, because hardening that breaks the business gets quietly removed, and quietly removed hardening protects nothing.
