# Credential Dumping Detection

## Objective

Detect attempts to extract credentials from memory.

## Tool

Mimikatz

## MITRE ATT&CK

T1003 - OS Credential Dumping

## Detection Sources

* Sysmon
* Wazuh
* Velociraptor

## Indicators

* LSASS access
* Suspicious process injection
* Memory access attempts

## Security Findings

Credential dumping behavior successfully detected.

## Response

Host isolated for investigation.

## Lessons Learned

Credential theft is a critical stage of many advanced attacks.
