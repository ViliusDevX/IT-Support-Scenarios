# Scenario 001: GPO Not Applying Due to Wrong OU

A newly prepared domain workstation was missing its expected standard configuration.

At first glance, the device looked healthy:

* Domain login worked
* Network access worked
* The GPO existed
* The GPO was linked to the correct OU

However, the policy still was not applying.

## Root Cause

`WIN11-CLIENT01` was placed in the `Staging` OU instead of the `Workstations` OU.

Because the workstation baseline GPO was linked to the `Workstations` OU, the computer object was outside the policy scope.

## Fix

Moved `WIN11-CLIENT01` back into the correct `Workstations` OU and refreshed computer Group Policy.

## Validation

Before the fix, the validation registry value was missing.

After the fix, the expected value appeared:

```text
HKLM\SOFTWARE\ViliusLab\IT001
GPOApplied = Applied
```

`gpresult` also confirmed that the workstation baseline GPO was applied.

## What This Scenario Shows

* Active Directory OU troubleshooting
* Group Policy scope validation
* `gpresult` usage
* Registry-based GPO validation
* Clear helpdesk-style documentation

## Scenario Files

* [Original Ticket](ticket.md)
* [Investigation](investigation.md)
* [User Communication](communication.md)
* [Screenshots](screenshots/)
