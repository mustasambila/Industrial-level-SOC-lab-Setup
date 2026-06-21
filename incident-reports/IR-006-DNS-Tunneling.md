# Incident Report IR-006

## Executive Summary

Suspicious DNS traffic patterns indicative of tunneling activity were observed.

## Incident Classification

Command and Control

## Severity

High

## Detection Source

* Zeek
* Suricata
* Wazuh

## MITRE ATT&CK

T1071.004 - DNS

## Indicators

* Excessive DNS requests
* Long domain names
* High entropy queries

## Analysis

Traffic patterns suggested possible covert communications over DNS.

## Containment

* Blocked suspicious domains
* Increased DNS monitoring

## Recovery

No evidence of successful data exfiltration identified.

## Lessons Learned

DNS remains a common channel for covert communications.
