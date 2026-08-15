# Week 3 - Enterprise Server Deployment and Operating System Installation

## Student Information
- **Name:** Renz Rouei Villegas
- **Course:** ITEP 414 - System Administration and Maintenance
- **Date:** August 15, 2026

## Project Overview
This project documents the deployment of an Ubuntu Server virtual machine for a startup environment. It covers installation, initial configuration, verification, BIOS/UEFI research, the Linux boot process, Windows Server Evaluation, and a comparison of Windows Server, Ubuntu Server, and Rocky Linux.

## Learning Objectives
- Install and configure Ubuntu Server in a virtual machine.
- Configure a hostname, administrative user, storage, networking, and OpenSSH.
- Verify hostname, IP addressing, internet connectivity, updates, and SSH.
- Explain BIOS and UEFI and the Ubuntu boot process.
- Compare major enterprise server operating systems.
- Produce reproducible technical documentation.

## Virtual Machine Specifications

| Component | Configuration |
|---|---|
| Name | Ubuntu-Server-Week03 |
| RAM | 4 GB minimum |
| CPU | 2 virtual processors |
| Storage | 40 GB |
| Network | NAT or Bridged if instructed |
| ISO | Ubuntu Server LTS |

## Installation Summary
Ubuntu Server is installed in a dedicated virtual machine. The required hostname is `server01`, a non-root administrative account is created, Guided - Use Entire Disk is used for storage, and OpenSSH Server is enabled.

## Configuration Summary
- Hostname: `server01`
- Administrative user: non-root account with sudo access
- Networking: DHCP unless otherwise instructed
- SSH: OpenSSH Server enabled
- Additional packages: none unless instructed

## Verification Results

Replace the placeholders below with your actual results and screenshots.

| Check | Command / Evidence | Result |
|---|---|---|
| Login | Successful console login | TODO |
| Hostname | `hostname` | TODO |
| IP address | `ip addr` | TODO |
| Internet | `ping -c 4 google.com` | TODO |
| Updates | `sudo apt update` and `sudo apt upgrade -y` | TODO |
| SSH | `systemctl status ssh` | TODO |

## BIOS vs UEFI Highlights
UEFI is the modern replacement for legacy BIOS. It is normally paired with GPT, supports modern large-disk layouts, provides a standardized boot manager, and supports Secure Boot. See `BIOS_vs_UEFI.pdf` for the full comparison.

## Boot Process Flowchart
![Ubuntu Boot Process](diagrams/BootProcessFlowchart.png)

`Power On -> BIOS/UEFI -> Boot Device Detection -> GRUB -> Linux Kernel -> init/systemd -> Services -> Login Prompt`

## Windows Server Evaluation
Windows Server Evaluation must be installed in a separate VM. Required evidence includes installation/setup, assigned computer name, administrator password setup (do **not** expose the password), and successful login.

## Enterprise OS Comparison
The project compares Windows Server, Ubuntu Server, and Rocky Linux in licensing, interface, package management, security, performance, enterprise use cases, advantages, and disadvantages.

## Challenges Encountered
Document only challenges that you actually encounter during the VM installations. Do not fabricate troubleshooting evidence.

## Reflection

Week 3 gave me a more practical view of how operating-system deployment fits into System Administration. Installing a server is not only about reaching the login screen. The deployment has to be planned, configured, verified, updated, secured, and documented so another administrator can understand the environment later. The Ubuntu Server activity connected several concepts that are easy to study separately, such as virtualization, hostnames, IP addressing, storage, user accounts, package updates, SSH, and the boot process.

The verification stage was especially useful because it showed why administrators should not assume that an installation is successful just because the system starts. Checking the hostname confirms the machine identity, checking the IP address confirms network configuration, ping verifies connectivity and name resolution, package updates confirm repository access, and the SSH service check confirms that remote administration is available. These checks form a simple deployment checklist that can prevent problems from being discovered much later.

The BIOS and UEFI comparison also helped me understand what happens before the operating system starts. UEFI is more suitable for modern systems because it works with current storage layouts and security features such as Secure Boot, while legacy BIOS remains important for understanding older hardware and troubleshooting compatibility.

Comparing Windows Server, Ubuntu Server, and Rocky Linux reinforced that server operating systems should be selected according to workload, licensing, support, security, and administrator experience. Windows Server fits Microsoft-centered environments, while Ubuntu and Rocky Linux provide different Linux enterprise approaches.

Overall, this project improved both my technical and documentation skills. A System Administrator needs to be able to reproduce a deployment, prove that it works, explain technical choices, and leave clear instructions for the next person who maintains the system.

## Repository Files
- `InstallationGuide.pdf`
- `ProfessionalInstallationManual.pdf`
- `BIOS_vs_UEFI.pdf`
- `OS_Comparison.pdf`
- `BootProcessFlowchart.pdf`
- `diagrams/BootProcessFlowchart.png`
- `screenshots/`
- `references/`
- `README.md`

## References
See `references/REFERENCES.md`.
