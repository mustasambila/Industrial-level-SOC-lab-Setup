# Incident Report IR-007

## Executive Summary

Simulated lateral movement activity was detected between internal systems.

## Incident Classification

Lateral Movement

## Severity

Critical

## Detection Source

* Wazuh
* Zeek
* Velociraptor

## MITRE ATT&CK

T1021 - Remote Services

## Indicators

* Remote logons
* SMB activity
* Administrative share access

## Analysis

The simulation demonstrated attacker movement following initial compromise.

## Containment

* Restricted network access
* Monitored privileged accounts

## Recovery

Network segmentation reviewed and validated.

## Lessons Learned

Lateral movement detection is essential for limiting attacker progression.
