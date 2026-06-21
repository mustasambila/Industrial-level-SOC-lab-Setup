# Threat Hunting Playbook: Lateral Movement

## Hunting Objective

Identify attacker movement between internal systems.

## Threat Hypothesis

An attacker may have gained access to one system and is attempting to move laterally throughout the environment.

## MITRE ATT&CK Mapping

Technique:
T1021

Tactic:
Lateral Movement

## Data Sources

* Wazuh
* Zeek
* Velociraptor
* Windows Security Logs

## Investigation Process

### Step 1

Review successful logon events.

### Step 2

Identify unusual SMB connections.

### Step 3

Review remote administration activity.

### Step 4

Investigate administrative share access.

Examples:

* ADMIN$
* C$
* IPC$

### Step 5

Review privilege escalation events.

## Indicators

* New internal connections
* Remote command execution
* Administrative share access
* Credential reuse

## Escalation Criteria

Escalate if:

* Multiple hosts are accessed
* Administrative credentials are used
* Remote execution is observed

## Expected Outcome

Identify compromised accounts and stop attacker movement before domain-wide compromise.
