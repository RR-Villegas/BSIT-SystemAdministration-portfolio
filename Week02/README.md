# Week 2 - Enterprise Infrastructure Planning for a Startup Company

## Student Information
- **Name:** Renz Rouei Villegas
- **Program:** Bachelor of Science in Information Technology (BSIT)
- **Course:** ITEP 414 - System Administration and Maintenance
- **Week:** 2
- **Date:** August 15, 2026

## Project Overview
This portfolio project presents an enterprise infrastructure plan for **NexaForge Software Solutions**, a fictional 20-employee software development startup. The company begins with no computers, server, network, internet infrastructure, or security policies, so the environment is designed from the ground up.

## Learning Objectives
- Analyze the IT requirements of a small organization.
- Prepare hardware, software, and network inventories.
- Design a logical enterprise network topology.
- Explain key System Administration roles.
- Recommend practical infrastructure, backup, security, and expansion controls.
- Document technical decisions clearly using Markdown and a formal report.

## Company Scenario
**Company:** NexaForge Software Solutions  
**Nature of Business:** Software development, cloud integration, and technical consulting.  
**Office:** Santa Cruz, Laguna, Philippines (fictional office)

| Department | Employees |
|---|---:|
| Information Technology | 5 |
| Human Resources | 4 |
| Finance | 5 |
| Sales | 6 |
| **Total** | **20** |

## Hardware Inventory Summary
The proposed environment uses **14 desktops, 8 business laptops, 1 server, 1 managed 48-port switch, 1 business router, 1 dedicated firewall, 2 Wi-Fi 6 access points, 1 NAS, 2 UPS units, 2 external backup drives, 2 network printers, and 22 monitors**.

## Software Inventory Summary
- Windows 11 Pro
- Ubuntu Server 26.04 LTS
- Microsoft 365 Apps
- Visual Studio Code
- Git
- GitHub Desktop
- Oracle VirtualBox
- Google Chrome
- Microsoft Defender
- AnyDesk
- 7-Zip

## Embedded Network Diagram
![Enterprise Network Diagram](diagrams/EnterpriseNetworkDiagram.png)

`Internet -> ISP Modem -> Router -> Firewall -> Managed Switch -> Departments / Server / NAS / Printer / Wireless AP`

## Technologies Used
Windows 11 Pro, Ubuntu Server, Git/GitHub, VS Code, VirtualBox, CAT6 Ethernet, managed switching, Wi-Fi 6, VLAN-ready design, NAS/off-site backup, MFA, and endpoint protection.

## IT Roles Researched
1. **Helpdesk Technician** - frontline user and endpoint support.
2. **Network Administrator** - routing, switching, wireless, connectivity, and network security.
3. **Linux System Administrator** - Linux server installation, maintenance, accounts, storage, services, and security.
4. **Cloud Administrator** - cloud identity, compute, storage, networking, monitoring, and governance.

## Infrastructure Recommendations
- Business-grade fiber internet with a secondary connection as the company grows.
- A moderate business server with ECC memory, redundant SSD storage, and room for virtualization.
- A **3-2-1 backup strategy** using NAS, rotated encrypted external media, and an off-site/cloud copy.
- Firewall, VLAN segmentation, MFA, encryption, patching, least privilege, and logging.
- Microsoft Defender as the Windows endpoint-protection baseline.
- Unique passwords/passphrases, password-manager use, and MFA for privileged/sensitive accounts.
- Capacity planning for approximately 30-40 employees.

## Challenges Encountered
### 1. Balancing cost and scalability
The design avoids unnecessary enterprise hardware while keeping enough capacity for growth.

### 2. Designing backup beyond a single storage device
A NAS alone is not sufficient, so the plan adds rotated offline media and an off-site copy.

### 3. Matching technology to department needs
Sales receives more mobile laptops, while HR and Finance use stable fixed workstations and controlled access.

## Reflection
Completing this infrastructure planning project helped me understand that system administration begins long before a server is installed or a cable is connected. The most important lesson I learned was that hardware, software, networking, security, documentation, and business requirements have to be planned as one system. A decision in one area affects the others. For example, choosing a managed switch is not only a hardware decision because it also supports network segmentation, future expansion, troubleshooting, and security.

The most challenging part was balancing the needs of four departments while keeping the design realistic for a startup with only twenty employees. It would have been easy to overdesign the environment with unnecessary enterprise equipment, or underdesign it and leave no room for growth. I had to think about which employees need fixed desktops, which roles benefit from laptops, how many switch ports are required, how backups should be separated, and how the server and network devices should be protected.

Planning before deployment is important because mistakes are much cheaper to correct on paper than after equipment has been purchased and configured. A clear infrastructure plan also gives administrators a reference for troubleshooting, upgrades, budgeting, and onboarding future IT staff. Documentation reduces guesswork and makes decisions easier to explain to management.

This project will help me become a better System Administrator because it trained me to think beyond individual devices. Instead of only asking whether a computer or server works, I now have to consider reliability, security, maintainability, scalability, and the needs of the people using the system. It also reinforced the importance of documenting technical decisions so another administrator can understand and continue the work.

## Project Files
- `EnterpriseInfrastructurePlan.pdf`
- `EnterpriseInfrastructurePlan.docx`
- `diagrams/EnterpriseNetworkDiagram.png`
- `diagrams/EnterpriseNetworkDiagram.pdf`
- `references/REFERENCES.md`
- `LinkedInPost.md`

## References
See [`references/REFERENCES.md`](references/REFERENCES.md).
