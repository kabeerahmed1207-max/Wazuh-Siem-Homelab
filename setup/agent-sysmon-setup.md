# Wazuh Agent + Sysmon Setup

## Overview
This document covers the installation of the Wazuh agent and Sysmon on the Windows endpoint for enhanced visibility.

## Components
- **Endpoint OS**: Windows 10 / 11
- **Wazuh Agent Version**: Matching the manager version
- **Sysmon**: Sysmon with SwiftOnSecurity configuration

## Installation Steps

### 1. Install Wazuh Agent
- Downloaded the Windows agent from the Wazuh dashboard
- Installed the agent using the manager IP
- Registered the agent successfully
- Verified the agent appears as **Active** in the Wazuh dashboard

### 2. Install Sysmon
- Downloaded Sysmon from Microsoft Sysinternals
- Applied the SwiftOnSecurity Sysmon configuration
- Started the Sysmon service
- Confirmed Sysmon events are being generated

### 3. Verification
- Checked that Sysmon Event ID 1 (Process Creation) events are reaching Wazuh
- Confirmed additional Windows event logs are being collected
- Agent health status: Active and reporting

## Benefits of Sysmon
- High-fidelity process creation logs
- Network connection visibility
- File creation and registry monitoring
- Better detection of suspicious PowerShell and living-off-the-land binaries

## Status
✅ Windows agent + Sysmon successfully deployed and reporting to Wazuh.
