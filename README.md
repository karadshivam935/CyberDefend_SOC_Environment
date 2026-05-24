


╔══════════════════════════════════════════════════════════════════╗
║          🛡️   CyberDefend_SOC_Environment 🛡️                    ║
║                                                                  ║
║        Security Monitoring • Threat Detection • SOC Lab          ║
║                                                                  ║
║                      👨‍💻 Author: Shivam Karad                     ║
╚══════════════════════════════════════════════════════════════════╝


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
📌 PROJECT OVERVIEW
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

The Wazuh SOC Home Lab project demonstrates the deployment,
configuration, and integration of multiple open-source cybersecurity
tools to simulate a real-world Security Operations Center (SOC)
environment.

This lab was designed to provide hands-on experience in:

✔️ Security Monitoring
✔️ Threat Detection
✔️ Incident Investigation
✔️ Log Analysis
✔️ SIEM Administration
✔️ Network Security Monitoring
✔️ Alert Correlation
✔️ Detection Engineering
✔️ Threat Hunting

The project uses the Wazuh SIEM/XDR platform as the central security
monitoring solution integrated with multiple defensive technologies.

🔧 Technologies Integrated:

➤ Wazuh SIEM/XDR
➤ Suricata IDS/IPS
➤ pfSense Firewall
➤ Sysmon
➤ VirusTotal
➤ File Integrity Monitoring (FIM)
➤ VMware Workstation

This environment demonstrates how enterprise SOC infrastructures
collect, correlate, and analyze security events from endpoints and
network devices in real time.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🏗️ LAB ARCHITECTURE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

The lab environment was deployed using VMware Workstation with
multiple virtual machines representing different infrastructure
components and attack scenarios.

┌───────────────────────────────────────────────────────────────┐
│                     🔹 WAZUH SERVER                           │
└───────────────────────────────────────────────────────────────┘

The Wazuh Server acts as the centralized SIEM platform.

Core Components:
• Wazuh Manager
• Wazuh Indexer
• Wazuh Dashboard

Responsibilities:
✔️ Centralized Log Collection
✔️ Event Correlation
✔️ Alert Generation
✔️ Threat Monitoring
✔️ Security Visualization

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

┌───────────────────────────────────────────────────────────────┐
│                 🔹 WINDOWS 11 ENDPOINT                        │
└───────────────────────────────────────────────────────────────┘

A Windows 11 Pro machine was configured as the monitored endpoint.

Key Features:
✔️ Wazuh Agent Deployment
✔️ Windows Event Log Collection
✔️ Sysmon Integration
✔️ File Integrity Monitoring
✔️ Real-Time Endpoint Visibility

The endpoint continuously forwards logs and telemetry data to the
Wazuh server for centralized analysis.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

┌───────────────────────────────────────────────────────────────┐
│                🔹 KALI LINUX ATTACKER MACHINE                 │
└───────────────────────────────────────────────────────────────┘

A Kali Linux VM was used to simulate attacker behavior.

Activities Performed:
⚔️ SSH Brute-Force Simulation using Hydra
⚔️ Network Scanning
⚔️ Threat Emulation
⚔️ Security Testing

This system helped validate the detection and monitoring capabilities
of the SOC environment.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

┌───────────────────────────────────────────────────────────────┐
│                    🔹 PFSENSE FIREWALL                        │
└───────────────────────────────────────────────────────────────┘

pfSense was deployed as the virtual firewall for the lab network.

Functions:
🛡️ Network Traffic Filtering
🛡️ Firewall Policy Enforcement
🛡️ Remote Log Forwarding
🛡️ Traffic Monitoring

Firewall logs were integrated into Wazuh to improve network
visibility and anomaly detection.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

┌───────────────────────────────────────────────────────────────┐
│                    🔹 SURICATA IDS/IPS                        │
└───────────────────────────────────────────────────────────────┘

Suricata was implemented to monitor malicious network activity.

Capabilities:
🔍 Intrusion Detection System (IDS)
🔍 Intrusion Prevention System (IPS)
🔍 Signature-Based Detection
🔍 Real-Time Traffic Inspection

Suricata alerts were forwarded to Wazuh for centralized monitoring
and alert correlation.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🛠️ WAZUH DEPLOYMENT & CONFIGURATION
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

📍 STEP 1 — WAZUH SERVER & AGENT SETUP

Objectives:
✔️ Deploy Wazuh using Official OVA
✔️ Configure Wazuh Services
✔️ Access Wazuh Dashboard
✔️ Register Endpoint Agents

Implementation Highlights:
➤ Installed Wazuh inside VMware
➤ Verified Manager, Dashboard & Indexer Services
➤ Configured Secure Agent Communication
➤ Centralized Endpoint Log Collection
➤ Tested Dashboard Visibility & Log Forwarding

This stage established the core SIEM infrastructure for the SOC lab.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🔌 SECURITY TOOL INTEGRATIONS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

📍 SURICATA INTEGRATION

Overview:
Suricata was integrated to provide network-based intrusion detection.

Key Implementations:
✔️ Installed Suricata with Npcap
✔️ Configured IDS & IPS Modes
✔️ Enabled Detection Rules
✔️ Monitored Suspicious Traffic
✔️ Forwarded Alerts to Wazuh

Outcome:
Centralized intrusion detection monitoring inside Wazuh Dashboard.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

📍 PFSENSE INTEGRATION

Overview:
pfSense firewall logs were integrated into Wazuh.

Key Implementations:
✔️ Configured Remote Syslog Forwarding
✔️ Sent Firewall Logs to Wazuh
✔️ Created Custom Rules & Decoders

Detection Capabilities:
🔹 Allowed Connections
🔹 Blocked Traffic
🔹 Authentication Events
🔹 Firewall Anomalies

Outcome:
Improved network visibility and event correlation.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

📍 VIRUSTOTAL INTEGRATION

Overview:
VirusTotal integration was configured for threat intelligence
enrichment.

Key Implementations:
✔️ Configured VirusTotal API
✔️ Enabled File Monitoring
✔️ Triggered Automatic Hash Lookups
✔️ Added Threat Reputation Data to Alerts

Outcome:
Enhanced malware investigation and faster alert triage.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

📍 FILE INTEGRITY MONITORING (FIM)

Overview:
Wazuh FIM was configured to monitor critical directories and files.

Key Features:
✔️ Real-Time File Monitoring
✔️ Recursive Directory Scanning
✔️ Change Detection
✔️ File Creation & Deletion Tracking

Outcome:
Improved endpoint visibility and tamper detection.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

📍 WINDOWS LOGS & SYSMON INTEGRATION

Overview:
Sysmon was deployed to improve endpoint telemetry and forensic
visibility.

Collected Events:
📄 Process Creation
📄 Network Connections
📄 Registry Changes
📄 Authentication Events
📄 File Modifications

Outcome:
Enhanced detection depth and advanced threat visibility.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🔐 BRUTE FORCE ATTACK SIMULATION & DETECTION
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

A controlled brute-force attack simulation was performed using Hydra
from the Kali Linux attacker machine.

Attack Activities:
⚔️ Multiple Failed Login Attempts
⚔️ SSH Authentication Attacks
⚔️ Realistic Brute-Force Patterns

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

📍 DETECTION & INVESTIGATION

Wazuh successfully detected:

✔️ Repeated Authentication Failures
✔️ Suspicious Login Activity
✔️ Brute-Force Attack Patterns

Important Windows Event IDs:
🔹 Event ID 4625 — Failed Login Attempt

Alert Correlation Identified:
➤ High-Frequency Failed Logins
➤ Suspicious IP Addresses
➤ Authentication Anomalies

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

📍 DEFENSIVE MEASURES IMPLEMENTED

🛡️ Strong Password Policies
🛡️ Multi-Factor Authentication (MFA)
🛡️ Account Lockout Policies
🛡️ Wazuh Active Response
🛡️ Firewall-Based Blocking

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
📊 SKILLS DEMONSTRATED
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

✔️ SIEM/XDR Deployment
✔️ Wazuh Administration
✔️ SOC Monitoring
✔️ Threat Detection
✔️ IDS/IPS Configuration
✔️ Firewall Log Analysis
✔️ Sysmon Deployment
✔️ Threat Intelligence Integration
✔️ File Integrity Monitoring
✔️ Incident Investigation
✔️ Rule Tuning & Decoders
✔️ Attack Simulation
✔️ VMware Virtualization
✔️ Network Security Monitoring

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🎯 PROJECT OUTCOME
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

This SOC Home Lab successfully replicated key functions of a modern
Security Operations Center using open-source technologies.

The environment demonstrated:

✔️ Centralized Security Visibility
✔️ Multi-Source Log Ingestion
✔️ Real-Time Alerting
✔️ Threat Detection Workflows
✔️ Security Event Investigation
✔️ Defensive Monitoring Capabilities

The integration of Wazuh, Suricata, pfSense, Sysmon, and VirusTotal
created a layered monitoring architecture capable of detecting both
endpoint and network-based threats.

The project also provided hands-on experience with realistic SOC
analyst responsibilities including:

🔎 Alert Triage
🔎 Threat Hunting
🔎 Detection Engineering
🔎 Log Investigation
🔎 Incident Analysis
🔎 Security Monitoring Operations

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
⚠️ ETHICAL USE NOTICE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

This project was created strictly for educational and defensive
security purposes inside an isolated lab environment.

All attack simulations and testing activities were performed only on
authorized systems owned within the lab infrastructure.

❌ Do NOT use these techniques against unauthorized or production
systems.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
👨‍💻 AUTHOR
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Shivam Karad
Cybersecurity Enthusiast | SOC & DFIR Learner | Security Monitoring

╔══════════════════════════════════════════════════════════════════╗
║                    🚀 END OF DOCUMENT 🚀                        ║
╚══════════════════════════════════════════════════════════════════╝
