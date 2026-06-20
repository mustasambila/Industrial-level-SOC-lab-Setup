# Wazuh SIEM Deployment Guide

## Overview

Wazuh serves as the central Security Information and Event Management (SIEM) platform within the SOC environment. It collects, analyzes, correlates, and visualizes security events from endpoints, network devices, and security tools.

## Objectives

* Centralized log management
* Security event monitoring
* Threat detection
* Incident response support
* Compliance monitoring

## Server Configuration

| Setting          | Value               |
| ---------------- | ------------------- |
| Operating System | Ubuntu Server 22.04 |
| RAM              | 8 GB                |
| CPU              | 4 vCPU              |
| Storage          | 100 GB              |
| IP Address       | 192.168.10.10       |

## Installation Steps

### System Update

sudo apt update

sudo apt upgrade -y

### Download Installer

curl -sO https://packages.wazuh.com/4.7/wazuh-install.sh

### Execute Installation

sudo bash ./wazuh-install.sh -a

## Components Installed

* Wazuh Manager
* OpenSearch
* Wazuh Dashboard
* Filebeat

## Dashboard Access

https://192.168.10.10

## Agent Registration

Endpoints registered:

* Windows 11
* Ubuntu Server
* Kali Linux

## Integrations

Integrated with:

* pfSense
* Suricata
* Zeek
* Sysmon
* Velociraptor

## Security Monitoring Capabilities

* Log Analysis
* File Integrity Monitoring
* Vulnerability Detection
* Malware Detection
* Threat Intelligence Correlation

## Outcome

Wazuh successfully deployed as the central monitoring and detection platform.
