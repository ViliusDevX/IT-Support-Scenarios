# Scenario 006: Remote PowerShell Connection Fails

`WIN11-CLIENT01` could be used locally, but IT could not manage it remotely with PowerShell.

At first glance, the workstation appeared normal:

* The device was online
* The user had no local workstation issue
* The hostname resolved
* The issue was limited to remote administration
* Other machines were not reported as affected

However, Remote PowerShell commands to the workstation failed.

## Root Cause

Windows Remote Management was not properly enabled on `WIN11-CLIENT01`.

The local investigation showed:

* `WinRM` service was stopped
* Windows Remote Management firewall rules were disabled
* Port `5985` was not accepting remote connections
* `Test-WSMan` and `Invoke-Command` failed from the admin machine

## Fix

Enabled PowerShell remoting on `WIN11-CLIENT01`.

This started the WinRM service and enabled the required Windows Remote Management firewall exception.

## Validation

After the fix, remote administration worked successfully:

* `Test-NetConnection` to port `5985` succeeded
* `Test-WSMan` returned a valid WinRM response
* `Invoke-Command` successfully returned the workstation hostname

## What This Scenario Shows

* Remote PowerShell troubleshooting
* WinRM service validation
* Windows Remote Management firewall rule review
* Port `5985` testing
* Separating local workstation health from remote administration failure
* Clear before-and-after validation

## Scenario Files

* [Original Ticket](ticket.md)
* [Investigation](investigation.md)
* [User Communication](communication.md)
* [Screenshots](screenshots/)
