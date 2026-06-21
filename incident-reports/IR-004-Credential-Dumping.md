# Incident Report IR-004

## Executive Summary

Credential dumping behavior was identified on a Windows endpoint through abnormal access to LSASS memory.

## Incident Classification

Credential Access

## Severity

Critical

## Detection Source

* Sysmon
* Wazuh
* Velociraptor

## MITRE ATT&CK

T1003 - OS Credential Dumping

## Indicators

* LSASS access attempts
* Suspicious memory operations
* Privilege escalation activity

## Analysis

A credential extraction simulation generated behavior consistent with common attacker tooling.

## Containment

* Isolated affected host
* Captured forensic artifacts
* Reviewed privileged accounts

## Recovery

No credentials were exfiltrated.

## Lessons Learned

Credential theft often precedes lateral movement and privilege escalation.
