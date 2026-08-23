# Windows Active Directory Home Lab

## Overview
This project is a self-built Windows Server Active Directory environment, created as hands-on practice to reinforce CompTIA Network+ and Security+ concepts and to build practical IAM/identity administration skills beyond day-to-day help desk work.

The lab was built from scratch on a MacBook (Apple Silicon) using UTM for virtualization, running Windows Server 2022 (Evaluation) as the domain controller.

## Why I Built This
I work in a customer service role handling password resets, MFA, and IAM support, and wanted to go deeper — understanding and administering the systems behind those processes rather than just the front-line tickets. This lab lets me practice the concepts I'm studying for Network+/Security+ in a real environment instead of only reading about them.

## Environment / Tools
- **Host:** MacBook (Apple Silicon — M-series)
- **Virtualization:** UTM
- **Server OS:** Windows Server 2022 (Evaluation)
- **Role(s) configured:** Active Directory Domain Services (AD DS)

## Architecture
```
[ Host: MacBook (Apple Silicon) ]
            |
        [ UTM Virtualization ]
            |
   [ Windows Server 2022 - Domain Controller ]
            |
      (Client VMs - planned/in progress)
```
*(Diagram to be expanded as client machines and additional roles are added.)*

## What I Configured
- Installed and set up Windows Server 2022 (Evaluation) as a virtual machine under UTM
- Promoted the server to a Domain Controller and configured Active Directory Domain Services
- **Domain:** `ayanna.local`
- **Organizational Unit (OU):** `IT-Staff`
- **Security Group:** `Help-Desk-Team`
- **User Account:** `Test User`
- **Domain-joined Computer:** `WIN-04P3NTJR3FF`
- [ Add: DNS configuration details ]
- [ Add: any Group Policy Objects (GPOs) configured ]

## Troubleshooting & Lessons Learned
- Initially attempted to install **Windows Server 2025 (Evaluation)**, but ran into a license validation failure preventing setup from completing.
- Resolved by falling back to **Windows Server 2022 (Evaluation)**, which installed and licensed successfully, allowing the project to proceed.
- *(This is a good example of real-world troubleshooting — documenting it shows problem-solving, not just a finished result.)*

## Skills Demonstrated
- Virtualization and VM management (UTM)
- Windows Server installation and licensing troubleshooting
- Active Directory Domain Services setup
- Identity and Access Management (IAM) fundamentals
- Foundational knowledge aligned with CompTIA Network+ and Security+ objectives

## Next Steps
- Add client VMs and join them to the domain
- Create Organizational Units (OUs), user accounts, and security groups
- Configure Group Policy Objects (GPOs) for security hardening
- Automate user/group creation using PowerShell (`New-ADUser`, `New-ADGroup`, etc.)
- Add screenshots of AD Users and Computers, Group Policy Management, and successful domain login

## Screenshots
*(Add screenshots here as the lab progresses — e.g., Server Manager, AD Users and Computers, DNS Manager, successful client login.)*

---
*This is an evolving project and will be updated as the lab grows (additional roles, PowerShell automation, and eventually integration with a cloud environment such as AWS).*
