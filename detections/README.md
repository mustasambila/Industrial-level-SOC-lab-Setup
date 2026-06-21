# Detection Engineering for SOC Operations

## Overview

This directory contains detection engineering resources developed for a Security Operations Center (SOC) home lab environment. The purpose of these resources is to demonstrate the development, testing, tuning, and deployment of detection logic using industry-standard frameworks and technologies.

The detection content is designed to support:

* Threat Hunting
* Security Monitoring
* Incident Response
* Adversary Emulation
* Detection Validation
* Threat Intelligence Integration

The project utilizes multiple detection technologies including:

* Wazuh Custom Rules
* Sysmon Event Monitoring
* Sigma Rules
* YARA Rules
* MITRE ATT&CK Mapping
* Threat Intelligence Correlation

---

## Detection Engineering Objectives

The primary objectives include:

### Visibility

Generate telemetry from endpoints, network devices, and security controls.

### Detection

Identify malicious activity using behavioral analytics and signature-based detections.

### Investigation

Provide actionable alerts with sufficient context for SOC analysts.

### Continuous Improvement

Reduce false positives while increasing detection coverage.

---

## Detection Sources

### Endpoint Telemetry

* Sysmon
* Windows Event Logs
* PowerShell Logs
* Security Event Logs

### Network Telemetry

* pfSense Firewall Logs
* Zeek Logs
* Suricata Alerts
* DNS Logs

### Security Platforms

* Wazuh SIEM
* Threat Intelligence Feeds

---

## Detection Categories

### Credential Access

Examples:

* Mimikatz execution
* LSASS access
* Credential dumping

### Execution

Examples:

* PowerShell abuse
* Command execution
* Script execution

### Persistence

Examples:

* Registry modifications
* Scheduled tasks
* Startup folder abuse

### Defense Evasion

Examples:

* Log clearing
* Security tool tampering
* AMSI bypass

### Lateral Movement

Examples:

* PsExec
* SMB abuse
* Remote PowerShell

### Impact

Examples:

* Ransomware encryption
* Data destruction
* Service disruption

---

## MITRE ATT&CK Alignment

All detections are mapped to the MITRE ATT&CK framework to ensure standardized threat coverage.

Examples:

* T1059 – Command and Scripting Interpreter
* T1003 – OS Credential Dumping
* T1021 – Remote Services
* T1486 – Data Encrypted for Impact
* T1505 – Server Software Component

---

## Repository Structure

detections/
├── custom-wazuh-rules.md
├── sigma-rules.md
├── yara-rules.md
├── sysmon-detection-usecases.md
├── mitre-attck-mapping.md
├── alert-correlation.md
├── false-positive-tuning.md
├── threat-intelligence-detection.md
├── powershell-detection.md
├── credential-dumping-detection.md
├── ransomware-detection.md
├── lateral-movement-detection.md
├── web-shell-detection.md

---

## Future Enhancements

* Machine Learning-Based Detection
* UEBA Integration
* Automated Incident Response
* Threat Intelligence Automation
* SOAR Playbooks

---

## Author

This project was developed as part of a SOC Home Lab environment to demonstrate practical detection engineering, threat hunting, and security monitoring capabilities using open-source technologies.
