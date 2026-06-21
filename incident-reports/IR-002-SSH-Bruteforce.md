# Incident Report IR-002

## Executive Summary

An SSH brute force attack was detected against a Linux server. The attack involved repeated authentication attempts using multiple password combinations.

## Incident Classification

Credential Access

## Severity

High

## Detection Source

* Wazuh
* Suricata
* pfSense

## MITRE ATT&CK

T1110 - Brute Force

## Indicators of Compromise

* Multiple failed login attempts
* Authentication failures
* Repeated connection requests

## Analysis

Hydra was used to perform password guessing attacks against the SSH service.

## Containment

* Blocked source IP
* Enabled additional monitoring
* Reviewed authentication logs

## Recovery

No successful compromise occurred.

## Lessons Learned

Rate limiting and MFA significantly reduce brute force risks.
