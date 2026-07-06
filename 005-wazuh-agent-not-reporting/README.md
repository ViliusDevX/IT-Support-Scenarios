# Scenario 005: Endpoint Monitoring Agent Not Reporting

`WIN11-CLIENT01` stopped reporting to the endpoint monitoring dashboard.

At first glance, the workstation appeared healthy:

* The workstation was online
* The DNS Client service was running
* The Wazuh agent service was installed and running
* Network connectivity to the monitoring server was available
* Another monitored endpoint was able to report normally

However, `WIN11-CLIENT01` still appeared disconnected in the Wazuh dashboard.

## Root Cause

`WIN11-CLIENT01` had a stale Wazuh manager IP address configured in its local agent configuration.

The Wazuh agent was still trying to report to the old manager IP:

`10.10.10.102`

The current Wazuh manager IP was:

`10.10.10.101`

Because of this, the agent service was running locally, but it was attempting to send check-ins and logs to the wrong monitoring server address.

## Fix

Updated the Wazuh agent configuration on `WIN11-CLIENT01` to use the current Wazuh manager IP address.

The configuration file was updated here:

`C:\Program Files (x86)\ossec-agent\ossec.conf`

After updating the manager IP, the Wazuh agent service was restarted.

## Validation

After the configuration was corrected and the service was restarted, `WIN11-CLIENT01` returned to active status in the Wazuh dashboard.

The Wazuh dashboard confirmed that the endpoint was reporting successfully again.

## What This Scenario Shows

* Endpoint monitoring agent troubleshooting
* Wazuh agent service validation
* Local agent configuration review
* Wazuh manager IP troubleshooting
* Agent log analysis
* Before-and-after dashboard validation
* Clear helpdesk-style documentation

## Scenario Files

* [Original Ticket](ticket.md)
* [Investigation](investigation.md)
* [User Communication](communication.md)
* [Screenshots](screenshots/)
