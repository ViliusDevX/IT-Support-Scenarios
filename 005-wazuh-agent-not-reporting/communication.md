# Endpoint Monitoring Agent Not Reporting

## Ticket Status

**Status:** Resolved

**Ticket ID:** IT-005

**Affected device:** WIN11-CLIENT01

**Affected system:** Wazuh / Endpoint monitoring

**Category:** Endpoint Monitoring / Agent Health

## User-Facing Reply

*Hello,*

*I checked the endpoint monitoring issue for `WIN11-CLIENT01` and confirmed that the workstation was online and the Wazuh agent service was running.*

*The issue was caused by the Wazuh agent still using an old manager IP address in its configuration. Because of this, the agent was attempting to report to the previous monitoring server address instead of the current Wazuh server.*

*I updated the Wazuh agent configuration to use the correct manager IP address and restarted the Wazuh service. After the change, I confirmed that `WIN11-CLIENT01` returned to active status in the Wazuh dashboard.*

*Thank you,*
*IT Support*
