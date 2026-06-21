# Threat Hunting Playbook: Ransomware Activity

## Hunting Objective

Identify ransomware behavior before widespread encryption occurs.

## Threat Hypothesis

An attacker may be preparing to encrypt files and impact business operations.

## MITRE ATT&CK Mapping

Technique:
T1486

Tactic:
Impact

## Data Sources

* Sysmon
* Wazuh
* Velociraptor

## Investigation Process

### Step 1

Review recent process creation events.

### Step 2

Identify mass file modification activity.

### Step 3

Review suspicious executable launches.

### Step 4

Investigate shadow copy deletion attempts.

### Step 5

Review persistence mechanisms.

## Indicators

* Rapid file modifications
* File extension changes
* Shadow copy deletion
* Backup tampering

## Escalation Criteria

Escalate immediately if:

* Encryption behavior observed
* Backup deletion attempts occur
* Multiple hosts show similar activity

## Expected Outcome

Early detection and containment of ransomware operations.
