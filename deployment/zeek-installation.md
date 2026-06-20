# Zeek Network Security Monitoring Deployment

## Overview

Zeek provides deep network visibility and protocol analysis for advanced threat hunting and incident investigations.

## Objectives

* Network metadata collection
* DNS monitoring
* HTTP monitoring
* SSL/TLS analysis
* Threat hunting

## Installation

Operating System:
Ubuntu Server 22.04

Installation Command:

sudo apt install zeek -y

## Monitored Protocols

* DNS
* HTTP
* HTTPS
* SSH
* FTP
* SMTP

## Generated Logs

* conn.log
* dns.log
* http.log
* ssl.log
* notice.log

## Integration

Logs forwarded into Wazuh for centralized analysis.

## Threat Hunting Use Cases

* DNS Tunneling
* Beaconing Detection
* Data Exfiltration
* Suspicious User Agents
* Lateral Movement

## Outcome

Zeek successfully deployed for advanced network visibility and threat hunting operations.
