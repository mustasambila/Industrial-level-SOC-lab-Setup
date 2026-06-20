# pfSense to Wazuh Integration

## Overview

The pfSense firewall is configured to forward security events and system logs to Wazuh using Syslog.

## Objectives

* Monitor firewall activity
* Detect blocked connections
* Monitor VPN events
* Analyze network traffic patterns

## Configuration

### pfSense

Navigate to:

Status → System Logs → Settings

Enable:

Remote Logging

Configure:

Remote Log Server:
192.168.10.10

Protocol:
UDP 514

### Wazuh

Configure Syslog listener on the Wazuh server.

Restart Wazuh Manager after configuration.

## Events Collected

* Firewall Blocks
* Firewall Allows
* VPN Connections
* DHCP Activity
* DNS Activity
* System Events

## Security Benefits

* Centralized log collection
* Firewall monitoring
* Network visibility
* Threat correlation

## Outcome

pfSense successfully forwards security logs into the Wazuh SIEM platform.
