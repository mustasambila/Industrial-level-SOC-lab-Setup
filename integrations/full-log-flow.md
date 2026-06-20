# Complete SOC Log Flow

## Enterprise SOC Architecture

Internet
↓
pfSense Firewall
↓
Suricata IDS/IPS
↓
Zeek Network Monitoring
↓
Wazuh SIEM
↓
TheHive Incident Response

## Endpoint Monitoring

Windows 11
↓
Sysmon
↓
Wazuh Agent
↓
Wazuh Manager

## Threat Intelligence

Threat Feeds
↓
MISP
↓
Wazuh

## Digital Forensics

Wazuh Alert
↓
Velociraptor Investigation
↓
Evidence Collection

## Incident Response Workflow

Detection
↓
Alert Correlation
↓
Threat Intelligence Enrichment
↓
Incident Creation
↓
Investigation
↓
Containment
↓
Recovery
↓
Lessons Learned

## Outcome

The integrated SOC platform provides end-to-end visibility across network, endpoint, threat intelligence, and incident response domains.
