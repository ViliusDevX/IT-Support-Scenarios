# New Workstation Missing Standard Configuration

## Ticket Status

**Status:** Resolved

**Ticket ID:** IT-001

**Affected device:** WIN11-CLIENT01

**Category:** Workstation / Group Policy

## User-Facing Reply

*Hello,*

*I checked `WIN11-CLIENT01` and confirmed that the workstation was joined to the domain and could communicate with the domain controller successfully.*

*The issue was caused by the workstation being placed in the wrong Active Directory location during setup. Because of that, it was outside the scope of the standard workstation policy, so the expected configuration was not being applied.*

*After moving the workstation into the correct `Workstations` OU, I confirmed that the device is now receiving the correct domain policy and the issue is fixed.*

*Thank you,
IT Support*
