# Network Reconnaissance Detection

## Objective

Simulate attacker reconnaissance activities and validate network visibility.

## Attack Tool

Nmap

## Attack Commands

nmap -sS 192.168.200.0/24

nmap -A 192.168.200.101

## MITRE ATT&CK

T1046 - Network Service Discovery

## Detection Sources

* Suricata IDS
* Zeek
* Wazuh

## Observed Indicators

* Multiple connection attempts
* Port enumeration
* Service fingerprinting

## Alert Generation

Suricata generated scanning alerts.

Zeek recorded connection metadata.

Wazuh correlated security events.

## Lessons Learned

Network scanning is often the first stage of an intrusion and should be monitored continuously.
