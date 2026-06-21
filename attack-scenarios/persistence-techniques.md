# Persistence Technique Detection

## Objective

Detect persistence mechanisms used by attackers.

## Techniques Tested

* Registry Run Keys
* Scheduled Tasks
* Startup Folder Persistence

## MITRE ATT&CK

T1547 - Boot or Logon Autostart Execution

## Detection Sources

* Sysmon
* Velociraptor
* Wazuh

## Indicators

* Registry modifications
* New scheduled tasks
* Startup artifacts

## Findings

Persistence mechanisms successfully detected.

## Lessons Learned

Persistence often indicates a compromised system requiring immediate investigation.
