# 🛡️ CyberDefend_SOC_Environment

<p align="center">
  <img src="https://img.shields.io/badge/Wazuh-SIEM-blue?style=for-the-badge">
  <img src="https://img.shields.io/badge/Suricata-IDS%2FIPS-red?style=for-the-badge">
  <img src="https://img.shields.io/badge/pfSense-Firewall-orange?style=for-the-badge">
  <img src="https://img.shields.io/badge/Sysmon-Windows%20Monitoring-green?style=for-the-badge">
</p>

<p align="center">
  <b>Security Monitoring • Threat Detection • SOC Operations • Incident Investigation</b>
</p>

---

# 👨‍💻 Author

**Shivam Karad**  
Cybersecurity Enthusiast | SOC & DFIR Learner

---

# 📌 Project Overview

This project demonstrates the deployment and integration of a complete **Security Operations Center (SOC) Home Lab** using open-source cybersecurity tools.

The lab simulates real-world SOC operations including:

- 📊 Log Collection
- 🚨 Threat Detection
- 🔍 Alert Investigation
- 🌐 Network Monitoring
- 🛡️ Incident Response
- 📁 File Integrity Monitoring
- 🧠 Threat Intelligence Enrichment

The environment is built around the **Wazuh SIEM/XDR platform** integrated with multiple defensive technologies.

---

# 🏗️ Lab Architecture

The SOC environment was deployed using **VMware Workstation** with multiple virtual machines representing enterprise infrastructure and attack scenarios.

## 🔹 Components Used

| Component | Purpose |
|----------|----------|
| 🖥️ Wazuh Server | Centralized SIEM/XDR Platform |
| 💻 Windows 11 Endpoint | Endpoint Monitoring & Log Collection |
| ⚔️ Kali Linux | Attack Simulation Machine |
| 🔥 pfSense Firewall | Firewall & Network Monitoring |
| 🕵️ Suricata IDS/IPS | Intrusion Detection & Prevention |
| 📄 Sysmon | Advanced Windows Telemetry |
| 🌍 VirusTotal | Threat Intelligence Enrichment |

---

# 🖥️ Wazuh Server

The Wazuh Server acts as the centralized SIEM platform.

## Core Components

- Wazuh Manager
- Wazuh Indexer
- Wazuh Dashboard

## Responsibilities

- Centralized Log Collection
- Event Correlation
- Alert Generation
- Threat Monitoring
- Security Visualization

---

# 💻 Windows 11 Endpoint

The Windows endpoint was configured with:

- Wazuh Agent
- Windows Event Log Collection
- Sysmon Integration
- File Integrity Monitoring (FIM)

## Features

✅ Real-Time Monitoring  
✅ Endpoint Visibility  
✅ Security Event Collection  
✅ Threat Detection Support  

---

# ⚔️ Kali Linux Attacker Machine

A Kali Linux VM was used to simulate attacker activity.

## Activities Performed

- SSH Brute-Force Simulation using Hydra
- Network Scanning
- Threat Emulation
- Security Testing

This system validated the detection capabilities of the SOC environment.

---

# 🔥 pfSense Firewall Integration

pfSense was deployed as the virtual firewall.

## Functions

- Network Traffic Filtering
- Firewall Policy Enforcement
- Remote Syslog Forwarding
- Traffic Monitoring

## Detection Visibility

- Allowed Connections
- Blocked Traffic
- Authentication Events
- Firewall Anomalies

---

# 🕵️ Suricata IDS/IPS Integration

Suricata was integrated for network intrusion detection.

## Capabilities

- Intrusion Detection System (IDS)
- Intrusion Prevention System (IPS)
- Signature-Based Detection
- Real-Time Traffic Inspection

## Outcome

Suricata alerts were forwarded into Wazuh for centralized monitoring and correlation.

---

# 🛠️ Wazuh Deployment & Configuration

## Step 1 — Wazuh Server & Agent Setup

### Objectives

- Deploy Wazuh using Official OVA
- Configure Wazuh Services
- Access Wazuh Dashboard
- Register Endpoint Agents

### Implementation Highlights

- Installed Wazuh inside VMware
- Verified Wazuh Services
- Configured Secure Agent Communication
- Centralized Endpoint Log Collection
- Tested Dashboard Monitoring

---

# 🔌 Security Tool Integrations

# 📍 Suricata Integration

## Key Implementations

- Installed Suricata with Npcap
- Configured IDS & IPS Modes
- Enabled Detection Rules
- Monitored Suspicious Traffic
- Forwarded Alerts to Wazuh

---

# 📍 pfSense Integration

## Key Implementations

- Configured Remote Syslog Forwarding
- Sent Firewall Logs to Wazuh
- Created Custom Decoders & Rules

---

# 📍 VirusTotal Integration

## Features

- VirusTotal API Integration
- Automatic Hash Reputation Lookup
- Malware Reputation Enrichment
- Faster Threat Investigation

---

# 📍 File Integrity Monitoring (FIM)

## Features

- Real-Time File Monitoring
- Recursive Directory Scanning
- File Change Detection
- Unauthorized Modification Alerts

---

# 📍 Sysmon & Windows Logs Integration

## Monitored Events

- Process Creation
- Network Connections
- File Modifications
- Registry Changes
- Authentication Events

## Outcome

Enhanced forensic visibility and advanced threat detection.

---

# 🔐 Brute Force Attack Simulation & Detection

A controlled brute-force attack simulation was performed using Hydra from the Kali Linux attacker machine.

## Attack Activities

- Multiple Failed Login Attempts
- SSH Authentication Attacks
- Brute-Force Simulation

## Wazuh Detection

Wazuh successfully detected:

- Repeated Authentication Failures
- Suspicious Login Attempts
- Brute-Force Attack Patterns

## Important Event IDs

| Event ID | Description |
|----------|-------------|
| 4625 | Failed Login Attempt |

---

# 🛡️ Defensive Measures Implemented

- Strong Password Policies
- Multi-Factor Authentication (MFA)
- Account Lockout Policies
- Wazuh Active Response
- Firewall-Based Blocking

---

# 📊 Skills Demonstrated

- SIEM/XDR Deployment
- Wazuh Administration
- SOC Monitoring
- Threat Detection
- IDS/IPS Configuration
- Firewall Log Analysis
- Sysmon Deployment
- Threat Intelligence Integration
- File Integrity Monitoring
- Incident Investigation
- Rule Tuning & Decoders
- Attack Simulation
- VMware Virtualization
- Network Security Monitoring

---

# 🎯 Project Outcome

This SOC Home Lab successfully replicated key functions of a modern Security Operations Center using open-source technologies.

## The environment demonstrated:

✅ Centralized Security Visibility  
✅ Multi-Source Log Ingestion  
✅ Real-Time Alerting  
✅ Threat Detection Workflows  
✅ Security Event Investigation  
✅ Defensive Monitoring Capabilities  

The integration of Wazuh, Suricata, pfSense, Sysmon, and VirusTotal created a layered monitoring architecture capable of detecting both endpoint and network-based threats.

---

# ⚠️ Ethical Use Notice

This project was created strictly for **educational and defensive security purposes** inside an isolated lab environment.

All attack simulations and testing activities were conducted only on authorized systems owned within the lab infrastructure.

> ❌ Do NOT use these techniques against unauthorized or production systems.

---

# 📂 Documentation

## Included Guides

- Wazuh Setup Guide
- Suricata Integration Guide
- pfSense Integration Guide
- VirusTotal Integration Guide
- File Integrity Monitoring Guide
- Sysmon Integration Guide
- Brute Force Detection Guide

---

<p align="center">
  <b>🛡️ Wazuh SOC Home Lab — Built for Learning, Monitoring & Threat Detection 🛡️</b>
</p>
