# THM-Summit-SOC-Detection-Lab
SOC analyst simulation focused on malware detection using hashes, IPs, DNS filtering, Sigma rules, host artifacts, and MITRE ATT&amp;CK mapping through the TryHackMe Summit room.
Overview

In this room, I acted as a Security Operations Center (SOC) analyst investigating a series of malware samples deployed by an adversary named Sphinx.

The objective was to detect and stop multiple malware variants using different detection strategies, including:

File Hash Detection
IP Address Blocking
DNS Domain Blocking
Host-Based Artifact Detection
Sigma Rule Creation
MITRE ATT&CK Mapping
Malware Behaviour Analysis

As the attacker evolved their techniques, traditional Indicators of Compromise (IOCs) became ineffective, requiring more advanced detection methods focused on behavior and persistence mechanisms.

Learning Objectives
Understand different types of Indicators of Compromise (IOCs)
Detect malware using file hashes
Detect malware using malicious IP addresses
Block malicious domains through DNS filtering
Investigate malware behavior in sandbox environments
Create Sigma detection rules
Map detections to MITRE ATT&CK techniques
Detect host-based persistence and defense evasion activity
Tools Used
PicoSecure Platform
Malware Sandbox
DNS Rule Manager
Sigma Rule Validator
MITRE ATT&CK Framework
Investigation Walkthrough
Sample 1 – File Hash Detection

Technique Used: Hash-Based Detection

Steps:

Analyzed sample1.exe
Identified malicious file hash
Created detection rule
Successfully blocked execution

Flag Obtained: ✅

Sample 2 – IP Address Detection

Technique Used: Network IOC Detection

Steps:

Investigated malware network activity
Identified Command & Control (C2) IP
Blocked malicious IP address
Prevented communication with attacker infrastructure

Flag Obtained: ✅

Sample 3 – DNS Detection

Technique Used: Malicious Domain Blocking

Findings:

Domain:
emudyn.bresonicz.info

Actions Taken:

Reviewed DNS requests
Identified malicious domain
Created DNS deny rule
Prevented malware communication

Flag Obtained: ✅

Sample 4 – Host Artifact Detection

Technique Used: Registry Monitoring

Malware Behaviour:

Disabled Windows Defender Real-Time Monitoring
Modified Registry Keys
Used Defense Evasion techniques

MITRE ATT&CK Mapping:

Technique	ATT&CK ID
Defense Evasion	TA0005

Detection Rule:

Registry Key Monitoring
Sigma Rule Validation

Flag Obtained: ✅

Sample 5 – Data Exfiltration Detection

Technique Used: File Creation Monitoring

Findings:

Malware created:

%temp%\exfiltr8.log

Observed Commands:

systeminfo
ipconfig /all
netstat -ano
net localgroup administrator

MITRE ATT&CK Mapping:

Technique	ATT&CK ID
Exfiltration	TA0010

Detection Strategy:

File Creation Monitoring
Sigma Rule Development
Behavioral Analysis

Flag Obtained: ✅

Key Takeaways

This room demonstrated why relying solely on traditional IOCs is not enough.

Attackers can easily:

Change file hashes
Rotate IP addresses
Register new domains

More resilient detections focus on:

Behavioral indicators
Registry modifications
Persistence mechanisms
Defense evasion activity
Data exfiltration patterns

This mirrors real-world SOC operations where analysts must continually adapt detection strategies as adversaries evolve.

MITRE ATT&CK Techniques Observed
Tactic	ID
Command and Control	TA0011
Defense Evasion	TA0005
Exfiltration	TA0010
Skills Practiced
Threat Hunting
IOC Analysis
Malware Analysis
Sigma Rule Creation
MITRE ATT&CK Mapping
DNS Security
SOC Investigation Workflow
