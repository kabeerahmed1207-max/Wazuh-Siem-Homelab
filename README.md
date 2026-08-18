# Exploring Wazuh – TryHackMe Lab Documentation

> Hands-on exploration of **Wazuh** (Open Source XDR + SIEM) using the official TryHackMe room  
> **Room**: [Exploring Wazuh](https://tryhackme.com/room/exploringwazuh)

---

## Why This Repository?

I originally planned to build a full **home lab** with Wazuh Manager + Indexer + Dashboard on a local VMware Kali Linux machine and install the Agent on Windows.  

Due to **hardware limitations** (insufficient RAM), running a complete local Wazuh deployment was not feasible.  

Instead, I used the official **TryHackMe “Exploring Wazuh”** room, which provides a pre-configured Wazuh environment. This repository documents everything I learned, explored, and practiced in that lab.

This approach still demonstrates practical understanding of Wazuh architecture, features, and SOC use cases.

---

## What is Wazuh?

Wazuh is a free and open-source security platform that unifies:

- **Endpoint Detection and Response (EDR / HIDS)**
- **SIEM** capabilities
- **Vulnerability Detection**
- **Configuration Assessment** (CIS Benchmarks)
- **File Integrity Monitoring (FIM)**
- **Log Analysis & Alerting**
- **Compliance reporting** (GDPR, HIPAA, NIST, PCI DSS, etc.)

It follows a classic **Manager + Agent** architecture.

### Architecture Overview

| Component          | Role                                      |
|--------------------|-------------------------------------------|
| **Wazuh Agent**    | Installed on endpoints (Windows/Linux/macOS). Collects logs, performs local checks, and sends data to the Manager. |
| **Wazuh Manager**  | Central orchestrator. Analyzes data, applies rules, generates alerts. |
| **Wazuh Indexer**  | Based on OpenSearch. Stores and indexes alerts for fast searching. |
| **Filebeat**       | Forwards data from Manager to Indexer. |
| **Wazuh Dashboard**| Web GUI (based on OpenSearch Dashboards) for visualization, investigation, and reporting. |

In the TryHackMe lab, all components run on a **single virtual machine**.

---

## Lab Environment (TryHackMe)

- Pre-deployed Wazuh management server
- Two agents already registered (Windows + Linux)
- Agents appear as **Disconnected** (expected in the lab)
- Login credentials provided in the room

---

## Topics Covered in This Lab

### 1. Agents & Agent Groups
- Viewing agent status and details
- Understanding agent groups for policy and log configuration
- Exploring agent inventory (CPU, OS, etc.)

### 2. IT Hygiene
- System information (hardware, network interfaces, OS)
- Installed software and packages
- Listening ports
- Local users and privileges

### 3. Configuration Assessment (CIS Benchmarks)
- Security hardening checks against CIS Benchmarks
- Scoring and identifying misconfigurations

### 4. Vulnerability Detection
- Scanning agents for known vulnerabilities (CVEs)
- Filtering by severity, package, and CVE ID
- Understanding the difference between reported vs. actually exploitable vulnerabilities

### 5. Logging & Log Analysis
- Using **Discover** to search raw events
- Understanding the difference between:
  - Raw logs
  - Decoders (parsing)
  - Rules (alerting)
  - Alerts (what appears in the dashboard)
- Searching authentication logs (SSH), Windows Defender events, etc.

### 6. Dashboards & Visualization
- Exploring pre-built dashboards
- Creating simple custom visualizations
- Using the Demo Dashboard

### 7. Advanced Concepts (Introduced)
- Agent configuration via Groups
- Decoders (how raw logs are parsed)
- Custom Rules (how alerts are generated)
- Active Response (automated actions on agents)
- File Integrity Monitoring (FIM)

---

## Key Takeaways

- Wazuh is much more than a simple HIDS — it is a full **XDR + SIEM** platform.
- The power of Wazuh comes from the combination of **Decoders + Rules**.
- Vulnerability Detection and CIS Configuration Assessment are extremely useful for GRC and IT teams.
- IT Hygiene gives excellent visibility into endpoint inventory.
- Proper agent grouping and custom log collection are essential for real SOC environments.

---

## Screenshots

*(Add your screenshots here in a `/screenshots` folder)*

- Overview page
- Agents list
- IT Hygiene view
- Vulnerability Detection results
- Discover search examples
- Demo Dashboard
- Rules / Decoders examples

---

## Future Plans

When hardware resources allow, I plan to:

- Deploy a full single-node Wazuh lab (Manager + Indexer + Dashboard)
- Install agents on Windows and Linux
- Create custom rules and Active Responses
- Simulate attacks and document detection

---

## References

- [TryHackMe – Exploring Wazuh](https://tryhackme.com/room/exploringwazuh)
- [Official Wazuh Documentation](https://documentation.wazuh.com)
- [Wazuh Website](https://wazuh.com)

---

**Disclaimer**: This repository is for educational purposes only. All hands-on work was performed in the official TryHackMe lab environment.
