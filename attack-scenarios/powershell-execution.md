# PowerShell Execution Detection

## Objective

Detect malicious PowerShell execution.

## Tool

Atomic Red Team

## Test Technique

T1059.001 - PowerShell

## Detection Sources

* Sysmon
* Wazuh

## Indicators

* powershell.exe execution
* Encoded commands
* Suspicious child processes

## Event Sources

Sysmon Event ID 1

Wazuh Security Alert

## Findings

Execution activity detected successfully and mapped to MITRE ATT&CK.

## Lessons Learned

PowerShell remains one of the most abused administrative tools in enterprise environments.
