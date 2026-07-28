# Wazuh SIEM Installation Guide

## Overview
This document describes the installation and initial configuration of the Wazuh SIEM server in my home lab environment using VMware.

## Lab Environment
- **Hypervisor**: VMware Workstation / Player
- **OS**: Ubuntu 24.04 LTS Server
- **Wazuh Version**: 4.x (All-in-One deployment)
- **Deployment Method**: Official Wazuh OVA / Assisted installation script

## Installation Steps

### 1. Create the Virtual Machine
- Allocated resources: 4–8 GB RAM, 2–4 vCPU, 50+ GB disk
- Network adapter: Host-Only / NAT (isolated lab network)
- Assigned static IP: `192.168.x.x`

### 2. Deploy Wazuh
- Downloaded the official Wazuh OVA (or used the assisted installation script)
- Imported the OVA into VMware
- Powered on the VM and completed initial setup

### 3. Access the Dashboard
- Accessed the Wazuh Dashboard via browser: `https://<Wazuh-IP>`
- Default credentials were changed immediately after first login
- Verified that Manager, Indexer, and Dashboard services were running

### 4. Post-Installation Checks
- Confirmed all Wazuh services are active
- Verified system resources and disk space
- Updated the system packages

## Notes
- The lab is completely isolated from the production network.
- Screenshots of the installation process are available in the `screenshots/` folder.

## Status
✅ Wazuh Server successfully deployed and accessible.
