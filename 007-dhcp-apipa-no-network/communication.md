# Workstation Has No Network Access

## Ticket Status

**Status:** Resolved

**Ticket ID:** IT-007

**Affected device:** WIN11-CLIENT01

**Affected resource:** Network connectivity

**Category:** DHCP / Networking

## User-Facing Reply

*Hello,*

*I checked the network access issue affecting `WIN11-CLIENT01` and confirmed that the workstation did not have a valid network configuration.*

*The device was using a link-local/APIPA address instead of receiving a normal DHCP address from the network. Because of this, it did not have a usable default gateway and could not reach internal resources, shared folders, or the internet.*

*I changed the IPv4 configuration back to automatic addressing and renewed the DHCP lease. After the change, the workstation received a valid IP address, gateway, and DNS server. I confirmed that internal network access, internet connectivity, and access to domain resources were restored.*

*Thank you,*

*IT Support*
