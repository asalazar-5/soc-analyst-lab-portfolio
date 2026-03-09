# Lab 02 – Port Scan Detection & Network Reconnaissance

## Objective

This lab demonstrates how network reconnaissance can be performed using Nmap and how a SOC analyst can identify open services running on a host.

The goal was to simulate attacker behavior by performing a port scan against a Windows system to enumerate exposed services.

---

## Tools Used

* Kali Linux
* Nmap
* VirtualBox
* Windows Host System

---

## Lab Environment

Attacker: Kali Linux VM
Target: Windows host machine running Splunk

---

## Step 1 – Identify Network Address

The Kali system IP address was identified using:

ip a

The Windows host IP address was identified using:

ipconfig

---

## Step 2 – Perform SYN Scan

The following command was used to perform a stealth SYN scan:

nmap -sS <target-ip>

This scan identifies open ports without completing the full TCP handshake.

---

## Step 3 – Service Enumeration

To identify running services, the following command was executed:

nmap -sV <target-ip>

This revealed several active services including:

135/tcp – Microsoft RPC
139/tcp – NetBIOS Session Service
445/tcp – Microsoft SMB
8000/tcp – Splunk Web Interface
8089/tcp – Splunk Management API

---

## Security Analysis

The scan identified several exposed services commonly found on Windows systems.

SMB and NetBIOS services are often targeted in lateral movement attacks, while exposed management interfaces such as Splunk could present administrative access points if improperly secured.

SOC analysts frequently monitor for port scanning behavior as it is often an early indicator of reconnaissance activity.

---

## Skills Demonstrated

Network reconnaissance
Port scanning detection
Service enumeration
Attack simulation in a controlled lab environment

---

## Screenshots

### Kali Linux IP Address
![Kali IP](screenshots/kali-ip.png)

### Windows Host IP Address
![Windows IP](screenshots/windows-ip.png)

### Nmap SYN Scan
![Nmap SYN Scan](screenshots/nmap-syn-scan.png)

### Nmap Service Detection Scan
![Nmap Service Scan](screenshots/nmap-service-scan.png)

### Windows Event Viewer Failed Logins
![Event Viewer Failed Logins](screenshots/event-viewer-failed-logins.png)
