# Lateral Movement Detection

## Objective

Detect movement between systems following compromise.

## Attack Techniques

* SMB Access
* Remote Command Execution
* Administrative Shares

## MITRE ATT&CK

T1021 - Remote Services

## Detection Sources

* Wazuh
* Zeek
* Velociraptor

## Indicators

* New SMB connections
* Remote logons
* Administrative access

## Findings

Movement between hosts detected and correlated.

## Lessons Learned

Lateral movement detection is critical for limiting attacker progression.
