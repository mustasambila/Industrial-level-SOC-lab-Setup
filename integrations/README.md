# Security Tool Integrations

## Overview

This section documents the integration of various security tools within the Enterprise SOC Home Lab.

The objective of these integrations is to centralize visibility, improve threat detection, enrich security events, and automate incident response workflows.

## Integrated Components

* pfSense Firewall
* Wazuh SIEM
* Suricata IDS/IPS
* Zeek Network Security Monitoring
* Sysmon
* Velociraptor
* MISP Threat Intelligence
* TheHive Incident Response Platform

## Security Monitoring Workflow

Network Traffic
→ pfSense
→ Suricata
→ Zeek
→ Wazuh

Endpoint Activity
→ Sysmon
→ Wazuh

Threat Intelligence
→ MISP
→ Wazuh

Incident Response
→ Wazuh
→ TheHive

DFIR
→ Velociraptor
→ Wazuh

The resulting architecture provides centralized monitoring, threat hunting, incident response, and forensic investigation capabilities.
