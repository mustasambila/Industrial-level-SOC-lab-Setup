# Suricata to Wazuh Integration

## Overview

Suricata alerts are forwarded into Wazuh for centralized monitoring and correlation.

## Objectives

* Detect malicious traffic
* Detect scanning activity
* Detect exploitation attempts
* Generate real-time alerts

## Integration Method

Suricata EVE JSON logs are forwarded to Wazuh.

Log Source:

eve.json

## Monitored Events

* Port Scanning
* Brute Force Activity
* Malware Traffic
* Command and Control Communication
* Exploit Attempts

## Alert Correlation

Wazuh correlates:

* Suricata Alerts
* Endpoint Events
* Firewall Logs

## Example Scenario

Nmap Scan

Detected by:

* Suricata

Correlated by:

* Wazuh

Mapped MITRE Technique:
T1046 Network Service Discovery

## Outcome

Suricata alerts are successfully visualized and correlated within Wazuh.
