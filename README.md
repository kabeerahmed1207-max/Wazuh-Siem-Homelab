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
- Exploring agent
