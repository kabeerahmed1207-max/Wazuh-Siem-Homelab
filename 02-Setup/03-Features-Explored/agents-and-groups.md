# Agents and Agent Groups

## Overview

Wazuh uses a **Manager–Agent** architecture.

- **Agent**: Lightweight software installed on endpoints (Windows, Linux, macOS). Collects logs, performs local checks, and sends data to the Manager.
- **Manager**: Central server that receives, analyzes, and generates alerts from agent data.

## In the Lab

The TryHackMe environment comes with **two agents** already registered:

- One Windows agent
- One Linux agent

Both agents show status as **Disconnected** (expected in this lab).

### Key Observations

- Agents can be organized into **Groups**.
- Groups allow different configurations (logging, policies, FIM settings) to be applied to specific sets of endpoints.
- Example groups: `default`, `CORP`, `BYOD`, `Windows-Servers`, `Linux-Workstations`.

### Agent Details Available

- OS version
- IP address
- Last keep-alive
- Agent version
- CPU and hardware information

## Takeaway

Proper agent grouping is essential in real environments for applying consistent monitoring policies across similar systems.
