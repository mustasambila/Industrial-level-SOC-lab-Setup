# Incident Report IR-001

## Executive Summary

A network reconnaissance activity was detected originating from a Kali Linux attack host. Multiple TCP connection attempts were observed against internal systems.

## Incident Classification

Reconnaissance Activity

## Severity

Medium

## Detection Source

* Suricata
* Zeek
* Wazuh

## MITRE ATT&CK

T1046 - Network Service Discovery

## Indicators

* High volume connection attempts
* Sequential port enumeration
* Service discovery behavior

## Analysis

The attacker performed active network reconnaissance using Nmap to identify exposed services and hosts within the environment.

## Containment

* Monitored source system
* Logged all connection attempts
* Generated SIEM alerts

## Lessons Learned

Reconnaissance is often the first stage of an attack and should trigger analyst review.
