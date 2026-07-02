# Unable to Access Department Shared Folder

## Ticket Status

**Status:** Resolved

**Ticket ID:** IT-002

**Affected device:** WIN11-CLIENT01

**Affected resource:** `\\DC01\Departments`

**Category:** File Share / Access Issue

## User-Facing Reply

*Hello,*

*I checked the department shared folder access issue and confirmed that the workstation could reach the file server successfully.*

*The shared folder itself was available, but the affected user account was not in the required access group for the department share. Because of that, Windows denied access to the folder.*

*After adding the account to the correct access group and refreshing the user's sign-in session, I confirmed that the department share can now be opened successfully.*

*Thank you,*
*IT Support*
