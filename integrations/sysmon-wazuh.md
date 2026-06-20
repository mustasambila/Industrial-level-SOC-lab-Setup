# Sysmon to Wazuh Integration

## Overview

Sysmon provides advanced Windows endpoint telemetry and forwards events to Wazuh.

## Objectives

* Process Monitoring
* Registry Monitoring
* Network Connection Monitoring
* Persistence Detection

## Configuration

Sysmon installed using SwiftOnSecurity configuration.

Events collected:

* Process Creation
* Network Connections
* Registry Modifications
* File Creation
* Driver Loading

## Wazuh Agent

The Wazuh Windows Agent collects Sysmon events from:

Applications and Services Logs/Microsoft/Windows/Sysmon/Operational

## Detection Examples

* PowerShell Abuse
* Credential Dumping
* Persistence Mechanisms
* Malware Execution

## MITRE ATT&CK Coverage

* Execution
* Persistence
* Discovery
* Credential Access

## Outcome

Sysmon endpoint telemetry successfully enriches Wazuh detection capabilities.
