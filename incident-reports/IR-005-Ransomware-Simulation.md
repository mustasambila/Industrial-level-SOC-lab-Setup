# Incident Report IR-005

## Executive Summary

A ransomware simulation was executed to validate endpoint detection and response capabilities.

## Incident Classification

Impact

## Severity

Critical

## Detection Source

* Sysmon
* Wazuh
* Velociraptor

## MITRE ATT&CK

T1486 - Data Encrypted for Impact

## Indicators

* Mass file modifications
* Encryption behavior
* Abnormal process execution

## Analysis

Behavior consistent with ransomware activity was successfully identified.

## Containment

* Host isolation
* Process termination
* Evidence collection

## Recovery

Files restored from backups.

## Lessons Learned

Behavioral detection is critical for ransomware defense.
