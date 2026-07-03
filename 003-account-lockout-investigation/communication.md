# User Account Keeps Locking Out

## Ticket Status

**Status:** Resolved

**Ticket ID:** IT-003

**Affected user:** `vilius\it003.user`

**Affected device:** WIN11-CLIENT01

**Category:** Account / Authentication Issue

## User-Facing Reply

*Hello,*

*I checked the account lockout issue for `vilius\it003.user` and confirmed that the account was being locked after repeated failed sign-in attempts.*

*The lockout events showed that the failed authentication attempts were coming from `WIN11-CLIENT01`. This was consistent with an old saved credential or another stale authentication attempt on the workstation using an incorrect password.*

*After clearing the incorrect authentication source on the workstation and unlocking the account, I confirmed that the user could sign in and access the required domain resources successfully.*

*Thank you,*
*IT Support*
