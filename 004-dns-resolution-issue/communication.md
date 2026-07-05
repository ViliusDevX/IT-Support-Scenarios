# Unable to Access Internal Resources by Name

## Ticket Status

**Status:** Resolved

**Ticket ID:** IT-004

**Affected device:** WIN11-CLIENT01

**Category:** Network / DNS Issue

## User-Facing Reply

*Hello,*

*I checked `WIN11-CLIENT01` and confirmed that the workstation had network and internet access, but internal resources were failing when accessed by name.*

*The issue was caused by the workstation using the wrong DNS server. It was pointed to the gateway DNS instead of the internal domain DNS server, so internal domain names were not resolving correctly.*

*After correcting the DNS server and clearing the DNS cache, I confirmed that internal resources can now be reached by name again.*

*Thank you,*
*IT Support*
