# DNS Tunneling Detection

## Objective

Detect covert communication through DNS.

## Attack Concept

Data transferred through DNS requests.

## Detection Sources

* Zeek
* Suricata
* Wazuh

## Indicators

* Excessive DNS queries
* Long domain names
* High entropy requests

## MITRE ATT&CK

T1071.004 - DNS

## Findings

Anomalous DNS activity identified through network telemetry.

## Lessons Learned

DNS traffic should be monitored as a potential command and control channel.
