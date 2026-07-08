# IT-Support-Scenarios

Realistic IT support and junior system administrator scenarios reproduced, investigated, and resolved in a home lab.

This repository is my practical IT support portfolio. Each scenario starts as a realistic support ticket, then documents the investigation process, root cause, fix, validation, screenshots, and final communication.

The goal is to show how I approach real technical problems: understand the issue, investigate carefully, fix the root cause, prove the result, and communicate clearly.

## Current Progress

**8 completed scenarios** covering common Windows, Active Directory, networking, permissions, remote administration, monitoring, and software installation issues.

| #   | Scenario                                                                      | Main Topic                        | Status    |
| --- | ----------------------------------------------------------------------------- | --------------------------------- | --------- |
| 001 | [GPO Not Applying Due to Wrong OU](001-gpo-not-applying-wrong-ou/)            | Active Directory / Group Policy   | Completed |
| 002 | [Network Share Access Denied](002-network-share-access-denied/)               | SMB / NTFS / AD Groups            | Completed |
| 003 | [Account Lockout Investigation](003-account-lockout-investigation/)           | Active Directory / Authentication | Completed |
| 004 | [DNS Resolution Issue](004-dns-resolution-issue/)                             | DNS / Domain Services             | Completed |
| 005 | [Wazuh Agent Not Reporting](005-wazuh-agent-not-reporting/)                   | Endpoint Monitoring               | Completed |
| 006 | [Remote PowerShell Connection Fails](006-winrm-remote-powershell-failure/)    | WinRM / Remote Administration     | Completed |
| 007 | [Workstation Has No Network Access](007-dhcp-apipa-no-network/)               | DHCP / APIPA / Networking         | Completed |
| 008 | [Unable to Install Required Software](008-software-install-permission-issue/) | Permissions / Software Install    | Completed |
| 009 | Print Spooler Service Failure                                                 | Windows Services / Printing       | Planned   |
| 010 | Slow Workstation Investigation                                                | Performance Troubleshooting       | Planned   |

## What This Project Demonstrates

This project focuses on practical troubleshooting skills used in helpdesk, desktop support, technical support, and junior system administrator roles.

It demonstrates experience with:

* Windows client troubleshooting
* Active Directory users, groups, and computer objects
* Group Policy scope and validation
* DNS and DHCP troubleshooting
* SMB shares, NTFS permissions, and access control
* Account lockout investigation
* WinRM and Remote PowerShell troubleshooting
* Endpoint monitoring agent checks
* Software installation permissions and approval flow
* PowerShell and command-line investigation
* Windows Event Viewer and log review
* Clear technical documentation
* User-facing support communication

## Support Workflow

Each scenario follows a realistic support workflow:

```text
User issue reported
        ↓
Original ticket created
        ↓
Issue reproduced in the lab
        ↓
Investigation and evidence collection
        ↓
Root cause identified
        ↓
Fix applied
        ↓
Validation performed
        ↓
User/internal communication written
```

This structure is intentional. I want each case to show not only the technical fix, but also how the issue was investigated and how the resolution would be communicated in a real support environment.

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

The lab is used as a controlled environment where I can create realistic problems, troubleshoot them safely, collect evidence, and document the full resolution process.

## Repository Structure

Each scenario usually follows this structure:

```text
00x-scenario-name/
├── README.md
├── ticket.md
├── investigation.md
├── communication.md
└── screenshots/
```

Some scenarios may include extra files when needed, for example:

```text
approval.md
```

This is used when a scenario includes approval or authorization, such as approved software installation.

## File Purpose

### `README.md`

A short polished summary of the scenario.

It explains the issue, root cause, fix, validation, and skills demonstrated.

### `ticket.md`

The original support ticket.

This file describes the issue from the user or business point of view. It does not include the solution, so the ticket stays realistic.

### `investigation.md`

The full troubleshooting process.

This file includes the lab reproduction, investigation steps, commands used, screenshots, findings, root cause, fix, and validation.

### `communication.md`

A realistic user-facing or internal support response.

This shows how the resolution would be explained clearly after the issue is fixed.

### `approval.md`

Optional file used when the scenario requires approval, authorization, or a change-control style note.

### `screenshots/`

Evidence collected during the investigation and validation process.

Screenshots are used to show the original problem, important checks, the fix, and proof that the issue was resolved.

## Scenario Highlights

### 001 - GPO Not Applying Due to Wrong OU

A workstation was not receiving its expected Group Policy settings because the computer object was placed in the wrong Active Directory OU.

Skills shown: OU placement, GPO scope, `gpresult`, registry-based validation.

### 002 - Network Share Access Denied

A user could reach a file share but was denied access because they were missing the required Active Directory security group membership.

Skills shown: SMB access, NTFS permissions, share permissions, group membership, logon token validation.

### 003 - Account Lockout Investigation

A domain account was repeatedly locking due to failed authentication attempts from a workstation.

Skills shown: account lockout troubleshooting, Event ID 4740, caller computer identification, credential cleanup.

### 004 - DNS Resolution Issue

A workstation had internet access but could not access internal resources by name because it was using the wrong DNS server.

Skills shown: DNS troubleshooting, `ipconfig`, `nslookup`, internal name resolution, AD DNS dependency.

### 005 - Wazuh Agent Not Reporting

A workstation stopped reporting to the monitoring dashboard because the local agent was configured with an outdated manager IP address.

Skills shown: service checks, agent configuration review, monitoring validation, dashboard confirmation.

### 006 - Remote PowerShell Connection Fails

A workstation was usable locally but could not be managed remotely because WinRM was not properly enabled.

Skills shown: WinRM, PowerShell remoting, firewall rules, port 5985 testing, `Test-WSMan`.

### 007 - Workstation Has No Network Access

A workstation had no usable network access because it had a link-local/APIPA address instead of a valid DHCP lease.

Skills shown: DHCP troubleshooting, APIPA identification, gateway/DNS validation, lease renewal.

### 008 - Unable to Install Required Software

A standard domain user could not install approved software because the installer required administrator approval.

Skills shown: local permissions, UAC, least privilege, approved installation process, post-install validation.

## Why I Built This

I created this repository to show practical IT support ability beyond just listing tools or certifications.

Each scenario is designed to show:

* How I read and understand a support ticket
* How I investigate without jumping straight to assumptions
* How I use Windows, AD, networking, and command-line tools
* How I identify the actual root cause
* How I validate that the fix worked
* How I communicate the resolution clearly

## Related Project

These scenarios are also connected to my broader IT and cybersecurity portfolio project:

[IT & Security Lab](https://vilius-lab.vercel.app/)

That project includes my learning journey, SOC practice scenarios, IT support cases, and interactive frontend work.

## Notes

All scenarios are performed in a controlled home lab environment. Names, systems, users, and resources are part of the lab setup and are used for learning and documentation purposes.
