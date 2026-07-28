# Incident Report – Brute Force Attempt

**Incident ID**: INC-001  
**Date**: [Add Date]  
**Severity**: Medium  
**Status**: Closed  

---

## 1. Summary
A brute-force login attempt was detected against a Windows endpoint in the home lab environment. The activity was identified by Wazuh through multiple failed authentication events.

## 2. Timeline
| Time          | Event                                      |
|---------------|--------------------------------------------|
| HH:MM         | First failed logon attempt observed        |
| HH:MM         | Multiple failed attempts in short period   |
| HH:MM         | Alert triggered in Wazuh                   |
| HH:MM         | Investigation completed                    |

## 3. Affected Asset
- Hostname: Windows-Endpoint
- IP Address: 192.168.x.x
- OS: Windows 10/11

## 4. Indicators of Compromise (IOCs)
- Multiple failed logon events (Event ID 4625)
- Targeted username: [Username]
- Source: Local / Lab network

## 5. MITRE ATT&CK
- T1110.001 – Brute Force: Password Guessing

## 6. Actions Taken
- Confirmed the activity was part of controlled testing
- Reviewed related authentication logs
- Documented the detection for portfolio purposes

## 7. Recommendations
- Enforce account lockout policies
- Enable stronger password requirements
- Monitor authentication anomalies continuously

## 8. Lessons Learned
This exercise helped practice real SOC workflows: alert triage, log correlation, MITRE mapping, and formal incident documentation.
