# Alejandro Salazar – Security Lab Portfolio

Welcome to my **Security Lab Portfolio**.
This repository contains hands-on cybersecurity labs aligned with **SOC Analyst, Security Analyst, and Blue Team roles**.

These labs demonstrate practical experience in:

* Security monitoring
* Threat detection and investigation
* Network reconnaissance
* Vulnerability assessment
* Threat hunting using SIEM tools

This portfolio reflects my transition from **enterprise IT support into cybersecurity**, combining 6+ years of IT experience with practical security investigations.

## Lab Environment Architecture

```
            ┌───────────────────────┐
            │      Kali Linux VM     │
            │  (Attacker / Scanner)  │
            │                        │
            │  - Nmap Recon         │
            │  - Vulnerability Scan │
            └───────────┬───────────┘
                        │
                        │ Network Traffic
                        │
            ┌───────────▼───────────┐
            │     Windows Host       │
            │     (Target System)    │
            │                        │
            │  - Authentication Logs │
            │  - Event Viewer Logs   │
            │  - Security Events     │
            └───────────┬───────────┘
                        │
                        │ Log Forwarding
                        │
            ┌───────────▼───────────┐
            │       Splunk SIEM      │
            │                        │
            │  - Log Ingestion       │
            │  - Threat Detection    │
            │  - Threat Hunting      │
            └───────────────────────┘
```

This lab simulates a basic **SOC monitoring environment** where security logs are generated on a Windows host, analyzed in Splunk, and investigated using threat hunting techniques. Kali Linux is used to perform reconnaissance, vulnerability scanning, and simulated attack activity.


---

# Labs Included

## 1. Log Analysis & Incident Detection

**Tools:** Splunk, Windows Security Logs

* Investigated Windows authentication logs
* Identified repeated failed login attempts
* Practiced SOC-style log analysis and alert triage

📁 Folder: `01-log-analysis`

---

## 2. Network Reconnaissance

**Tools:** Kali Linux, Nmap

* Performed host discovery and port scanning
* Identified exposed services on a target system
* Practiced enumeration techniques used during security assessments

📁 Folder: `02-network-reconnaissance`

---

## 3. Brute Force Attack Detection

**Tools:** Windows Event Viewer, Splunk

* Simulated repeated failed login attempts
* Analyzed Windows Event ID **4625** authentication failures
* Identified brute force patterns in authentication logs

📁 Folder: `03-brute-force-detection`

---

## 4. Vulnerability Scanning & Risk Analysis

**Tools:** Kali Linux, Nmap Vulnerability Scripts

* Conducted vulnerability scans against a target host
* Identified exposed services and potential vulnerabilities
* Reviewed CVE references and assessed risk severity

📁 Folder: `04-vulnerability-scanning`

---

## 5. Threat Hunting Investigation (Splunk)

**Tools:** Splunk, Windows Security Logs

* Performed threat hunting using SIEM queries
* Investigated suspicious authentication activity
* Identified unusual login behavior through event analysis

📁 Folder: `05-threat-hunting-splunk`

---

# Skills Demonstrated

* Security event monitoring and log analysis
* Threat detection and investigation
* Network reconnaissance and enumeration
* Vulnerability scanning and risk analysis
* Threat hunting using SIEM tools (Splunk)
* Security documentation and reporting

---

# Certifications

* CompTIA Network+
* CompTIA Security+

---

# About Me

I am an IT professional with **6+ years of experience supporting enterprise and educational environments**. I am currently transitioning into cybersecurity with a focus on **SOC Analyst and Security Analyst roles**.

My background includes:

* Endpoint and network troubleshooting
* Identity and access management
* Security event investigation
* Collaboration with engineering and security teams in regulated environments

This portfolio demonstrates my commitment to **continuous learning and practical cybersecurity skill development**.

