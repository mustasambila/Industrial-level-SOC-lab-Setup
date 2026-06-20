# Zeek to Wazuh Integration

## Overview

Zeek provides network metadata and protocol analysis which is forwarded into Wazuh.

## Objectives

* Improve network visibility
* Support threat hunting
* Detect anomalous activity
* Analyze DNS and HTTP traffic

## Log Sources

* conn.log
* dns.log
* http.log
* ssl.log
* notice.log

## Integration Method

Zeek logs are ingested by Wazuh through local file monitoring.

## Security Use Cases

* DNS Tunneling Detection
* Beaconing Detection
* Suspicious Domains
* Data Exfiltration
* Malware Communications

## Benefits

Unlike IDS alerts, Zeek provides rich network context and behavioral visibility.

## Outcome

Zeek network telemetry is available inside Wazuh dashboards and threat hunting workflows.
