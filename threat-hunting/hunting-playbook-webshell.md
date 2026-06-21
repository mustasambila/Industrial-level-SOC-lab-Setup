# Threat Hunting Playbook: Web Shell Activity

## Hunting Objective

Identify web shell uploads and post-exploitation activity on web servers.

## Threat Hypothesis

An attacker may have uploaded a malicious web shell following exploitation of a web application.

## MITRE ATT&CK Mapping

Technique:
T1505.003

Tactic:
Persistence

## Data Sources

* Web Server Logs
* Wazuh
* Sysmon
* File Integrity Monitoring

## Investigation Process

### Step 1

Review newly created files.

### Step 2

Search for:

* .php
* .aspx
* .jsp

files uploaded recently.

### Step 3

Review unusual HTTP requests.

### Step 4

Investigate command execution patterns.

### Step 5

Review outbound network connections.

## Indicators

* Unexpected PHP files
* Command execution requests
* Web server spawned processes
* Suspicious outbound traffic

## Escalation Criteria

Escalate if:

* Command execution is observed
* Web shell artifacts are discovered
* Persistence mechanisms exist

## Expected Outcome

Identify and remove attacker web shells before additional compromise occurs.
