# SSH Brute Force Detection

## Objective

Validate detection of password guessing attacks.

## Attack Tool

Hydra

## Attack Command

hydra -l root -P rockyou.txt ssh://192.168.200.101

## MITRE ATT&CK

T1110 - Brute Force

## Detection Sources

* Suricata
* Wazuh
* Syslog

## Indicators

* Multiple failed logins
* Rapid authentication attempts
* Repeated username targeting

## Security Events

Suricata generated brute force alerts.

Wazuh detected authentication failures.

pfSense logged repeated connections.

## Containment

Source IP blocked using pfSense firewall.

## Lessons Learned

Failed authentication events should be monitored and correlated automatically.
