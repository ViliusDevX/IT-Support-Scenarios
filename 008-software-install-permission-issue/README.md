# Scenario 008: Unable to Install Required Software

`vilius\it008.user` could sign in and use `WIN11-CLIENT01`, but could not install required software.

At first glance, the workstation appeared healthy:

* The user could sign in normally
* The workstation was online
* Network access was working
* The installer downloaded successfully
* The issue only appeared when the user tried to install the application

The installation failed because Windows required administrator approval.

## Root Cause

`vilius\it008.user` was a standard domain user and was not a member of the local Administrators group on `WIN11-CLIENT01`.

The software installer required elevated permissions, so the user could not complete the installation alone.

## Fix

Confirmed that the requested software was approved for installation.

The application was then installed using administrator approval, without granting the user permanent local administrator rights.

## Validation

After installation, the application was confirmed under:

`C:\Program Files\7-Zip`

Functionality was also tested by creating a small test archive.

The user remained a standard domain user after the installation.

## What This Scenario Shows

* Software installation permission troubleshooting
* Local administrator group review
* UAC / administrator approval handling
* Least-privilege support approach
* Approved software installation process
* Before-and-after validation
* Clear helpdesk-style documentation

## Scenario Files

* [Original Ticket](ticket.md)
* [Approval Note](approval.md)
* [Investigation](investigation.md)
* [User Communication](communication.md)
* [Screenshots](screenshots/)
