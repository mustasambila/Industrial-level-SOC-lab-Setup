# Incident Report IR-003

## Executive Summary

Suspicious PowerShell activity was detected on a Windows endpoint through Sysmon and Wazuh monitoring.

## Incident Classification

Execution

## Severity

High

## Detection Source

* Sysmon
* Wazuh

## MITRE ATT&CK

T1059.001 - PowerShell

## Indicators

* powershell.exe execution
* Suspicious command line parameters
* Script execution activity

## Analysis

An Atomic Red Team simulation executed PowerShell commands commonly associated with attacker activity.

## Containment

* Investigated host
* Reviewed parent processes
* Collected forensic evidence

## Recovery

System remained operational.

## Lessons Learned

PowerShell activity requires continuous monitoring due to its frequent use in attacks.
