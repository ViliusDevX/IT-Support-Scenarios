# Ticket: Remote PowerShell connection fails to workstation

## Ticket Details

**Ticket ID:** IT-006

**Priority:** Medium

**Category:** Remote Administration

**Affected device:** WIN11-CLIENT01

**Affected service:** WinRM / Remote PowerShell

**Reported by:** IT Support

**Status:** Open

## Original Request

Hello,

We are unable to connect to `WIN11-CLIENT01` using Remote PowerShell.

The workstation appears to be online, and the user has not reported any issue using the computer locally. However, when IT tries to run a remote PowerShell session or remote command against the device, the connection fails.

Remote administration is working for other workstations, so this appears to be limited to `WIN11-CLIENT01`.

Could someone please check why remote PowerShell access is not working for this workstation?

## Reported Symptoms

* Device name: `WIN11-CLIENT01`
* Workstation appears to be online
* User can work locally on the device
* Remote PowerShell connection fails
* Other workstations can be managed remotely
* Issue appears limited to this workstation

## Business Impact

IT cannot remotely manage or troubleshoot the workstation using standard PowerShell remoting tools. This may require manual access to the device if the issue is not resolved.

## Additional Notes

Please verify whether the workstation is reachable on the network and whether the required remote management services and firewall rules are configured correctly.
