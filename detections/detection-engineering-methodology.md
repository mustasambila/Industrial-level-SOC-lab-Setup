# Detection Engineering Methodology

## Overview

Detection Engineering is the process of designing, developing, testing, deploying, and continuously improving security detections that identify malicious activity within an organization's environment.

The goal of detection engineering is not simply to generate alerts but to create high-fidelity detections that accurately identify adversary behavior while minimizing false positives.

This methodology provides a structured approach for building detections within a Security Operations Center (SOC) using technologies such as Wazuh, Sysmon, Sigma, YARA, Zeek, Suricata, Windows Event Logs, and Threat Intelligence platforms.

---

# Detection Engineering Lifecycle

A mature detection engineering program follows a continuous lifecycle.

```text
Threat Intelligence
        ↓
Adversary Research
        ↓
Log Source Analysis
        ↓
Detection Development
        ↓
Testing & Validation
        ↓
Deployment
        ↓
Alert Triage
        ↓
False Positive Tuning
        ↓
Detection Improvement
        ↓
Repeat
```

---

# Phase 1: Threat Intelligence Collection

## Purpose

Threat intelligence provides information regarding:

* Emerging threats
* Malware campaigns
* Advanced Persistent Threats (APTs)
* Indicators of Compromise (IOCs)
* Adversary Tactics, Techniques, and Procedures (TTPs)

## Sources

### Open Source Intelligence (OSINT)

Examples:

* CISA Advisories
* MITRE ATT&CK
* Malware Bazaar
* AlienVault OTX
* AbuseIPDB
* VirusTotal

### Commercial Intelligence

Examples:

* Recorded Future
* CrowdStrike Intelligence
* Mandiant Intelligence
* Microsoft Threat Intelligence

---

# Phase 2: Adversary Research

## Purpose

Understand how attackers operate.

Instead of detecting malware names, detection engineers focus on attacker behavior.

### Example

Detecting:

```text
mimikatz.exe
```

is weak.

Detecting:

```text
LSASS memory access
Credential dumping behavior
Unauthorized privilege escalation
```

is stronger.

---

## ATT&CK-Based Research

Analyze attacker techniques using MITRE ATT&CK.

Examples:

### Credential Access

```text
T1003
OS Credential Dumping
```

### PowerShell

```text
T1059.001
PowerShell
```

### Lateral Movement

```text
T1021
Remote Services
```

### Ransomware

```text
T1486
Data Encrypted for Impact
```

---

# Phase 3: Log Source Analysis

## Purpose

Determine whether telemetry exists to detect the behavior.

Detection quality depends on log quality.

---

## Windows Event Logs

Examples:

### Security Logs

Event IDs:

```text
4624 - Successful Login
4625 - Failed Login
4672 - Privileged Logon
4688 - Process Creation
```

---

## Sysmon

Provides enhanced visibility.

### Common Sysmon Event IDs

| Event ID | Description           |
| -------- | --------------------- |
| 1        | Process Creation      |
| 3        | Network Connection    |
| 7        | Image Loaded          |
| 8        | Create Remote Thread  |
| 10       | Process Access        |
| 11       | File Create           |
| 13       | Registry Modification |
| 22       | DNS Query             |

---

## Network Logs

Examples:

### Zeek

* conn.log
* dns.log
* http.log
* ssl.log

### Suricata

* alerts
* signatures
* protocol analysis

### pfSense

* firewall logs
* blocked traffic
* connection attempts

---

# Phase 4: Detection Development

## Purpose

Transform threat intelligence into actionable detections.

---

## Detection Types

### Signature-Based Detection

Examples:

```text
Known hashes
Known domains
Known IP addresses
Known filenames
```

Advantages:

* Fast
* Accurate

Disadvantages:

* Easy to evade

---

### Behavioral Detection

Examples:

```text
PowerShell downloads content
Encoded commands
Credential dumping activity
Persistence mechanisms
```

Advantages:

* More resilient
* Detects unknown threats

Disadvantages:

* Requires tuning

---

### Anomaly Detection

Examples:

```text
Unusual login location
Abnormal process execution
Large data transfers
```

Advantages:

* Detects novel attacks

Disadvantages:

* Higher false positives

---

# Phase 5: Detection Validation

## Purpose

Verify detections trigger correctly.

---

## Testing Methods

### Atomic Red Team

Simulates ATT&CK techniques.

Examples:

```text
T1003
Credential Dumping

T1059
PowerShell

T1021
Remote Services
```

---

### Adversary Emulation

Examples:

* Caldera
* Infection Monkey
* Prelude Operator

---

### Manual Testing

Examples:

```powershell
powershell -enc <base64>
```

```cmd
rundll32.exe
```

```cmd
psexec.exe
```

---

# Phase 6: Detection Deployment

## Wazuh

Deploy:

```xml
local_rules.xml
```

---

## Sigma

Deploy:

```yaml
Sigma Rules
```

Convert using:

```bash
sigmac
```

---

## YARA

Deploy:

```bash
yara rules.yar sample.exe
```

---

# Phase 7: Alert Triage

Analysts should validate:

### True Positive

Malicious activity confirmed.

### False Positive

Legitimate activity incorrectly flagged.

### Benign Positive

Expected administrative activity.

---

## Triage Process

```text
Alert
 ↓
Context Gathering
 ↓
Threat Validation
 ↓
Containment
 ↓
Investigation
 ↓
Closure
```

---

# Phase 8: False Positive Tuning

## Purpose

Reduce alert fatigue.

---

### Techniques

Whitelist:

```text
Known Administrators
Known Scripts
Known Applications
```

Exclude:

```text
Backup software
Patch management tools
Monitoring agents
```

---

## Example

Instead of:

```text
Any PowerShell Execution
```

Detect:

```text
Encoded PowerShell Commands
PowerShell Download Activity
PowerShell Bypass Techniques
```

---

# Phase 9: Detection Metrics

Measure effectiveness.

---

## Detection Coverage

Questions:

* Which ATT&CK techniques are covered?
* Which techniques remain uncovered?

---

## Mean Time to Detect (MTTD)

Measures:

```text
Attack Start
↓
Detection Trigger
```

---

## Mean Time to Respond (MTTR)

Measures:

```text
Detection
↓
Containment
```

---

## False Positive Rate

Formula:

```text
False Positives
----------------
Total Alerts
```

---

# Detection Maturity Levels

## Level 1

Basic IOC detections.

Examples:

* IP addresses
* Domains
* Hashes

---

## Level 2

Behavior-based detections.

Examples:

* PowerShell abuse
* Registry persistence

---

## Level 3

Correlation detections.

Examples:

```text
PowerShell
+
Network Connection
+
Credential Access
```

---

## Level 4

Threat Intelligence Driven Detection.

Examples:

* IOC enrichment
* Threat actor mapping

---

## Level 5

Advanced Analytics.

Examples:

* Machine Learning
* UEBA
* Risk-Based Alerting

---

# Best Practices

1. Focus on attacker behavior.
2. Map detections to MITRE ATT&CK.
3. Validate detections continuously.
4. Monitor false positives.
5. Use multiple telemetry sources.
6. Document all detection logic.
7. Integrate threat intelligence.
8. Perform regular threat hunting.
9. Automate testing where possible.
10. Continuously improve coverage.

---

# Conclusion

Detection engineering is a continuous process that transforms threat intelligence and telemetry into actionable security detections. Effective detection engineering combines visibility, threat intelligence, behavioral analytics, validation, and continuous tuning to provide a robust defense against modern cyber threats.

The ultimate objective is to identify adversary behavior as early as possible while minimizing noise and maximizing analyst efficiency.
