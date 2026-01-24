# Lab 02 – Firewall Configuration & Network Security (SOC / Security Analyst Focus)

## Objective
The goal of this lab is to demonstrate hands-on experience configuring firewall rules, enforcing least-privilege network access, and validating security controls through traffic analysis. This lab mirrors real-world SOC and Security Analyst tasks related to network security monitoring and prevention.

---

## Tools Used
- pfSense Firewall
- Kali Linux
- Windows or Linux Virtual Machine
- Nmap (for traffic and port scanning)

---

## Lab Environment
- pfSense VM acting as the firewall
- One internal Windows/Linux VM behind the firewall
- Kali Linux VM simulating external traffic
- Virtual network configured to route traffic through pfSense

---

## Step-by-Step Implementation

### Step 1: Deploy pfSense Firewall
1. Install pfSense in a virtual machine.
2. Configure WAN and LAN interfaces.
3. Verify internal machines route traffic through pfSense.

📸 **Screenshot:** pfSense dashboard showing active interfaces.

---

### Step 2: Establish Baseline Connectivity
1. From the internal VM, verify internet connectivity.
2. From Kali Linux, verify access to the firewall IP.
3. Document baseline allowed traffic.

📸 **Screenshot:** Successful ping or connectivity test.

---

### Step 3: Configure Firewall Rules
1. Create firewall rules to:
   - Allow HTTP/HTTPS traffic (ports 80, 443)
   - Block unnecessary services (SSH, RDP)
2. Apply rules using a least-privilege approach.
3. Ensure rule order enforces proper priority.

📸 **Screenshot:** Firewall rules table in pfSense.

---

### Step 4: Validate Rules Using Port Scanning
1. From Kali Linux, run Nmap scans against the internal VM.
2. Verify:
   - Allowed ports are accessible
   - Blocked ports are denied
3. Confirm firewall behavior matches expectations.

📸 **Screenshot:** Nmap scan results showing blocked and allowed ports.

---

### Step 5: Analyze Firewall Logs
1. Review pfSense logs for blocked connection attempts.
2. Identify:
   - Source IP addresses
   - Target ports
   - Time of attempted access
3. Correlate scan activity with firewall log entries.

📸 **Screenshot:** Firewall logs showing denied traffic.

---

## Findings
- Firewall rules successfully restricted unnecessary services.
- Blocked traffic attempts were clearly logged and traceable.
- Network segmentation reduced attack surface.

---

## Lessons Learned
- Firewall rule order is critical for proper enforcement.
- Least-privilege network access significantly reduces risk.
- Log analysis is essential for validating security controls.

---

## Security+ Alignment
- Network security and segmentation
- Firewall configuration and monitoring
- Access control and least privilege
- Log review and security validation

---

## Interview Talking Points
- “I configured pfSense firewall rules to enforce least-privilege access.”
- “I validated firewall effectiveness using Nmap scanning from an external system.”
- “I analyzed firewall logs to confirm blocked traffic and identify potential threats.”
- “This lab reflects how SOC teams verify and monitor network security controls.”

---

## Next Steps
- Add IDS/IPS functionality (Snort or Suricata).
- Create alerts for repeated blocked connection attempts.
- Correlate firewall logs with SIEM data.


