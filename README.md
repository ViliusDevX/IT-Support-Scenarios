# IT-Support-Scenarios

This repository contains realistic IT support scenarios that I reproduced, investigated, and solved in my home lab.

The goal of this project is to show practical troubleshooting skills in a format that is close to real helpdesk, IT support, and junior system administrator work.

Each scenario starts with a support ticket and then documents the investigation, root cause, fix, validation, screenshots, and final communication.

## Lab Environment

The scenarios are reproduced in my Purple Team Home Lab.

The lab includes:

* Windows Server / Domain Controller
* Windows client workstation
* Active Directory
* Group Policy
* DNS and DHCP
* SMB file shares
* pfSense
* Wazuh
* Kali Linux

The lab is used as a realistic environment where issues can be created, tested, troubleshot, and resolved.

## Repository Structure

Each scenario follows this structure:

```text
00x-scenario-name/
├── README.md
├── ticket.md
├── investigation.md
├── communication.md
└── screenshots/
```

## How Each Scenario Is Organized

### `README.md`

A short summary of the scenario.

It explains the issue, root cause, fix, validation, and skills demonstrated.

### `ticket.md`

The original support ticket.

This file describes the problem from the user or business point of view. It does not include the solution, so it stays realistic.

### `investigation.md`

The full troubleshooting process.

This file includes how the issue was reproduced in the lab, what checks were performed, commands used, screenshots, findings, root cause, fix, and validation steps.

When relevant, it also links back to the related Purple Team Home Lab documentation.

### `communication.md`

A realistic ticket update or user-facing response.

This shows how the issue would be explained after resolution, including what was fixed and any recommended next steps.

### `screenshots/`

Evidence from the investigation and validation process.

## Scenarios


| Scenario                                    | Topic                             |  Status  |
| ------------------------------------------- | --------------------------------- | -------- |
| 001-gpo-not-applying-wrong-ou               | Active Directory / Group Policy   | Finished |
| 002-network-share-access-denied             | SMB / NTFS / AD Groups            | Finished |
| 003-account-lockout-investigation           | Active Directory / Authentication | Finished |
| 004-dns-resolution-issue                    | DNS / Domain Services             | Finished |
| 005-wazuh-agent-not-reporting               | Monitoring / Endpoint Agent       | Finished |
| 006-winrm-remote-powershell-failure         | Remote Administration             |  Planned |
| 007-dhcp-apipa-no-network                   | DHCP / Networking                 |  Planned |
| 008-software-install-permission-issue       | Permissions / Software Install    |  Planned |
| 009-print-spooler-service-failure           | Windows Services / Printing       |  Planned |
| 010-slow-workstation-investigation          | Performance Troubleshooting       |  Planned |


## Skills Demonstrated

This project demonstrates practical experience with:

* Windows troubleshooting
* Active Directory and Group Policy
* DNS, DHCP, and basic networking
* SMB shares and NTFS permissions
* User and group management
* PowerShell and command-line tools
* Windows event logs
* Endpoint monitoring
* Remote support troubleshooting
* Technical documentation
* User communication

## Purpose

This repository is my practical IT support portfolio.

Instead of only listing tools or certifications, these scenarios show how I approach real technical problems: understand the issue, investigate it, identify the root cause, apply a fix, validate the result, and communicate the resolution clearly.
