# Threat Hunting

## Overview

Threat hunting is a proactive cybersecurity activity focused on identifying adversary behaviors that may bypass traditional detection mechanisms.

Unlike alert-driven investigations, threat hunting begins with a hypothesis and uses available telemetry to validate or reject that hypothesis.

This section contains hunting methodologies and operational playbooks used within the Enterprise SOC Home Lab.

## Objectives

* Identify malicious activity before alerts are generated
* Validate detection coverage
* Improve visibility gaps
* Reduce attacker dwell time
* Strengthen incident response readiness

## Data Sources

The following telemetry sources are utilized during threat hunting operations:

* Wazuh SIEM
* Sysmon
* Zeek
* Suricata
* pfSense
* Velociraptor

## Hunting Workflow

1. Create a hunting hypothesis
2. Identify relevant data sources
3. Search for suspicious indicators
4. Correlate findings across systems
5. Validate malicious activity
6. Develop new detections
7. Document findings

## Hunting Playbooks

This repository currently includes:

* PowerShell Abuse Hunting
* Lateral Movement Hunting
* Ransomware Hunting
* Web Shell Hunting

## Expected Outcome

The threat hunting process improves SOC visibility and enables proactive detection of attacker techniques mapped to the MITRE ATT&CK framework.
