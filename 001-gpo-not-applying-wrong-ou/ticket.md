# Ticket: New workstation missing standard configuration

## Ticket Details

**Ticket ID:** IT-001
**Priority:** Medium
**Category:** Workstation / Group Policy
**Affected device:** WIN11-CLIENT01
**Reported by:** Helpdesk / User Onboarding
**Status:** Open

## Original Request

Hello,

We are preparing a new workstation for a user, but it looks like the standard workstation settings are not being applied.

The computer is joined to the domain and we are able to sign in with a domain account. Internet and shared resources seem to work, but one of the normal baseline settings that should appear on domain workstations is missing.

I already tried signing out and back in, but the setting still does not show up.

Could someone please check why this workstation is not getting the correct domain policy?

## Reported Symptoms

* Device name: `WIN11-CLIENT01`
* User can sign in with a domain account
* Network access appears to be working
* Standard workstation configuration is missing
* Issue appears limited to this workstation
* Other domain workstations appear to be working normally

## Business Impact

This workstation is being prepared for a user and should not be handed over until the standard domain configuration is applied.

## Additional Notes

This may be related to Group Policy, but I am not sure. Please verify whether the workstation is receiving the correct computer policies.
