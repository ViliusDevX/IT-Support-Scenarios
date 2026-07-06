# Ticket: Endpoint monitoring agent not reporting

## Ticket Details

**Ticket ID:** IT-005

**Priority:** Medium

**Category:** Endpoint Monitoring / Agent Health

**Affected device:** WIN11-CLIENT01

**Affected system:** Wazuh / Endpoint monitoring

**Reported by:** IT / Security Monitoring

**Status:** Open

## Original Request

Hello,

`WIN11-CLIENT01` is showing as disconnected in the endpoint monitoring dashboard.

The workstation appears to be online and no user-facing outage has been reported, but the monitoring console has not received recent agent check-ins from this device.

Other monitored systems appear to be reporting normally.

Could someone please check why this workstation is no longer reporting to monitoring?

## Reported Symptoms

* Device name: `WIN11-CLIENT01`
* Device appears to be online
* User has not reported a workstation issue
* Monitoring dashboard shows the endpoint as disconnected or inactive
* Other agents appear to be reporting normally
* Issue appears limited to this workstation

## Business Impact

The workstation is missing from normal endpoint monitoring visibility. If the issue remains unresolved, IT and security staff may not receive logs or alerts from this device.

## Additional Notes

Please verify whether the monitoring agent is installed, running, and able to communicate with the monitoring server.
