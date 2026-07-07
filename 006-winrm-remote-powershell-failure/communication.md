# Remote PowerShell Connection Fails to Workstation

## Ticket Status

**Status:** Resolved

**Ticket ID:** IT-006

**Affected device:** WIN11-CLIENT01

**Affected service:** WinRM / Remote PowerShell

**Category:** Remote Administration

## User-Facing Reply

*Hello,*

*I checked the Remote PowerShell issue affecting `WIN11-CLIENT01` and confirmed that the workstation was online and usable locally.*

*The issue was caused by Windows Remote Management not being properly enabled on the device. The `WinRM` service was stopped, and the Windows Remote Management firewall rules were disabled, which prevented remote PowerShell connections from reaching the workstation.*

*I enabled PowerShell remoting, which started the WinRM service and enabled the required firewall exception. After the change, I confirmed that remote PowerShell access to `WIN11-CLIENT01` was working successfully.*

*Thank you,*

*IT Support*
