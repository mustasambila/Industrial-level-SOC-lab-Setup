# Suricata IDS/IPS Deployment Guide

## Overview

Suricata provides network intrusion detection and intrusion prevention capabilities within the SOC environment.

## Objectives

* Detect malicious traffic
* Prevent attacks
* Generate security alerts
* Support threat hunting

## Deployment Location

Installed directly on pfSense.

## Installation Procedure

1. Login to pfSense.
2. Navigate to System > Package Manager.
3. Search for Suricata.
4. Install package.

## Interface Monitoring

Enabled Interfaces:

* WAN
* LAN

## Rule Sources

Enabled:

* Emerging Threats Open

## IPS Configuration

Enabled:

* Inline IPS Mode
* Promiscuous Mode

## Alert Categories

* Port Scanning
* Brute Force
* Malware Traffic
* Command and Control
* Exploit Attempts

## Log Forwarding

Alerts forwarded to:

* Wazuh SIEM

## Testing

Simulated attacks:

* Nmap Scan
* Hydra Brute Force
* Metasploit Exploitation

## Outcome

Suricata successfully deployed for network threat detection and prevention.
