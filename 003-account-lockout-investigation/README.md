# Scenario 003: Account Lockout Investigation

A domain user kept getting locked out during the workday.

At first glance, the issue looked user-specific:

* The user account existed in Active Directory
* The workstation was online
* The user could sign in after being unlocked
* Other users were not reporting the same issue
* The department share was accessible when valid credentials were used

However, the account continued to lock after repeated failed authentication attempts.

## Root Cause

`WIN11-CLIENT01` was repeatedly attempting to authenticate as `vilius\it003.user` with an incorrect password.

The domain controller Security log showed Event ID `4740`, with `WIN11-CLIENT01` listed as the caller computer.

The behavior was consistent with a stale saved credential, old mapped drive, script, or background SMB connection using the wrong password.

## Fix

Cleared the incorrect authentication source on `WIN11-CLIENT01`, removed existing SMB sessions where needed, and unlocked the user account in Active Directory.

## Validation

After the stale authentication source was cleared and the account was unlocked, the user could access the department share successfully:

```text
\\DC01\Departments
```

The expected file was visible:

```text
department-info.txt
```

## What This Scenario Shows

* Active Directory account lockout troubleshooting
* Domain lockout policy review
* Windows Security event log investigation
* Event ID `4740` analysis
* SMB authentication testing
* Clear helpdesk-style documentation

## Scenario Files

* [Original Ticket](ticket.md)
* [Investigation](investigation.md)
* [User Communication](communication.md)
* [Screenshots](screenshots/)
