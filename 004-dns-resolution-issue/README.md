# Scenario 004: DNS Resolution Issue

A workstation had working internet access, but internal domain resources failed when accessed by name.

At first glance, the device looked mostly healthy:

* Windows sign-in worked
* Internet access worked
* The DNS Client service was running
* The domain controller was reachable by IP address

However, internal names such as the domain controller hostname and `vilius.lab` were not resolving correctly.

## Root Cause

`WIN11-CLIENT01` was using the wrong DNS server.

The workstation was pointed to pfSense / gateway DNS:

```text
10.10.10.1
```

Instead of the internal Active Directory DNS server:

```text
10.10.10.10
```

Because Active Directory resources depend on internal DNS records, internet access still worked, but internal domain name resolution failed.

## Fix

Changed the workstation DNS server back to the internal AD DNS server and flushed the DNS cache.

## Validation

After the fix, `ipconfig /all` showed the correct DNS server:

```text
10.10.10.10
```

Internal DNS lookups and hostname tests worked again.

## What This Scenario Shows

* DNS troubleshooting
* Difference between internet connectivity and internal name resolution
* `ipconfig`, `nslookup`, and `ping` usage
* Active Directory DNS dependency
* Clear helpdesk-style documentation

## Scenario Files

* [Original Ticket](ticket.md)
* [Investigation](investigation.md)
* [User Communication](communication.md)
* [Screenshots](screenshots/)
