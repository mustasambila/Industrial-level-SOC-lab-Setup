# Web Enumeration Detection

## Objective

Detect web application reconnaissance activity.

## Attack Tools

* Gobuster
* Dirb

## Attack Commands

gobuster dir -u http://target -w common.txt

dirb http://target

## MITRE ATT&CK

T1595 - Active Scanning

## Detection Sources

* Zeek
* Wazuh
* Web Server Logs

## Indicators

* High volume requests
* Discovery of hidden directories
* Abnormal HTTP requests

## Findings

Enumeration activity identified through HTTP logs and request patterns.

## Lessons Learned

Web enumeration often precedes exploitation attempts.
