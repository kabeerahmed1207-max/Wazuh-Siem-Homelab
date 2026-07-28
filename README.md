# 🛡️ Wazuh SIEM Home Lab – SOC Portfolio Project

A hands-on Security Operations Center (SOC) home lab built with **Wazuh SIEM** on VMware.  
This project demonstrates endpoint monitoring, threat detection, log analysis, and incident response workflows commonly used by SOC Analysts.

---

## 🎯 Project Objectives

- Deploy and configure a fully functional Wazuh SIEM environment
- Onboard Windows (and Linux) endpoints with Wazuh agents + Sysmon
- Simulate real-world attacks and validate detections
- Map alerts to the **MITRE ATT&CK** framework
- Practice alert triage and write professional incident reports

---

## 🏗️ Lab Architecture

| Component            | Role                          | OS                  | IP Address (Lab)   |
|----------------------|-------------------------------|---------------------|--------------------|
| Wazuh Server         | Manager + Indexer + Dashboard | Ubuntu 24.04        | 192.168.x.x        |
| Windows Endpoint     | Monitored agent + Sysmon      | Windows 10/11       | 192.168.x.x        |
| Kali Linux (optional)| Attacker machine              | Kali Linux          | 192.168.x.x        |

> **Network**: Isolated Host-Only / NAT network on VMware  
> **Hypervisor**: VMware Workstation / Player

<!-- Add your network diagram later -->
<!-- ![Architecture Diagram](architecture/network-diagram.png) -->

---

## 🛠️ Technologies Used

- **SIEM**: Wazuh (Manager, Indexer, Dashboard)
- **Endpoint Visibility**: Sysmon (SwiftOnSecurity configuration)
- **Virtualization**: VMware
- **Attack Simulation**: Manual techniques + optional Metasploit
- **Framework**: MITRE ATT&CK

---

## 🔍 Detections Implemented

| Attack Technique              | MITRE ATT&CK     | Detection Method                    | Severity |
|-------------------------------|------------------|-------------------------------------|----------|
| Brute Force Login             | T1110.001        | Failed logon events (4625)          | Medium   |
| Local Account Creation        | T1136.001        | Event ID 4720 / 4732                | High     |
| Suspicious PowerShell         | T1059.001        | Sysmon Event ID 1 + custom rule     | High     |
| File Integrity Monitoring     | T1565 / T1070    | Wazuh FIM                           | Critical |
| Defense Evasion (Agent stop)  | T1562.001        | Wazuh agent status                  | Medium   |

---

## 📁 Repository Structure

wazuh-siem-homelab/
├── README.md
├── LICENSE
├── .gitignore
├── architecture/
│   └── network-diagram.png
├── setup/
│   ├── wazuh-installation.md
│   └── agent-sysmon-setup.md
├── detections/
│   ├── 01-brute-force.md
│   ├── 02-privilege-escalation.md
│   └── 03-powershell.md
├── incident-reports/
│   └── sample-incident-01.md
├── screenshots/
└── configs/



## 📝 Key Skills Demonstrated

- SIEM deployment and configuration (Wazuh)
- Endpoint monitoring with Sysmon
- Detection engineering & rule validation
- MITRE ATT&CK mapping
- Log analysis and alert triage
- Incident documentation and reporting
- Virtualized lab design (VMware)


## 🚀 Future Improvements

- [ ] Custom Wazuh rules & decoders
- [ ] Integration with Suricata / pfSense
- [ ] Automated response playbooks
- [ ] Additional attack simulations (lateral movement, etc.)

## 📄 License

This project is licensed under the **MIT License** – see the [LICENSE](LICENSE) file for details.
