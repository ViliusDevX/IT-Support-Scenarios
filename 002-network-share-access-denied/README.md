# Scenario 002: Network Share Access Denied

A domain user could sign in normally and reach the file server, but opening the department share returned an access denied message.

At first glance, the environment looked healthy:

* Domain login worked
* Network access worked
* The server name resolved
* The share was online
* Other users could access the same folder

However, this user still could not open the department share.

## Root Cause

The affected user was not a member of the required Active Directory security group for the `Departments` share.

Because the share and NTFS permissions were assigned through group membership, the user was denied access until the correct group membership was added.

## Fix

Added the user to the correct department access group and refreshed the user's logon session.

## Validation

After the group membership change and a new sign-in, the user could access:

```text
\\DC01\Departments
```

Group membership was also confirmed from the client using `whoami /groups`.

## What This Scenario Shows

* SMB share access troubleshooting
* NTFS and share permission validation
* Active Directory group membership checks
* User logon token awareness
* Clear helpdesk-style documentation

## Scenario Files

* [Original Ticket](ticket.md)
* [Investigation](investigation.md)
* [User Communication](communication.md)
* [Screenshots](screenshots/)
