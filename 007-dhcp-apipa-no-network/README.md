# Scenario 007: Workstation Has No Network Access

`WIN11-CLIENT01` could be used locally, but it had no usable network access.

At first glance, the issue looked workstation-specific:

* The user could sign in to Windows
* Other workstations were working normally
* Internet access was not working
* Internal resources were not reachable
* Shared folders could not be opened

The investigation focused on the workstation IPv4 configuration, DHCP lease status, gateway, and DNS settings.

## Root Cause

`WIN11-CLIENT01` was using a link-local/APIPA-style address instead of a valid DHCP lease.

The workstation had:

* IPv4 address in the `169.254.x.x` range
* No usable default gateway
* No working internal or internet connectivity

Because the workstation did not have a valid network configuration, it could not reach the default gateway, domain controller, DNS server, internal resources, or the internet.

## Fix

Changed the IPv4 settings back to automatic addressing and renewed the DHCP lease.

After the fix, the workstation received a valid network configuration:

* IP address: `10.10.10.100`
* Default gateway: `10.10.10.1`
* DNS server: `10.10.10.10`

## Validation

After renewing the DHCP lease, connectivity was restored.

Confirmed successful access to:

* Default gateway
* Domain controller / DNS server
* Internet IP address
* Internal domain DNS
* SYSVOL domain share

Internal resource access was validated with:

`\\vilius.lab\SYSVOL`

## What This Scenario Shows

* DHCP troubleshooting
* APIPA / link-local address identification
* IPv4 configuration review
* Gateway and DNS validation
* `ipconfig`, `ping`, and `nslookup` troubleshooting
* Separating local sign-in from network connectivity
* Clear before-and-after validation

## Scenario Files

* [Original Ticket](ticket.md)
* [Investigation](investigation.md)
* [User Communication](communication.md)
* [Screenshots](screenshots/)
