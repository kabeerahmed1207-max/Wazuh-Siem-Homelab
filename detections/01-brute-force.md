# Detection: Brute Force Login Attempt

## Summary
Simulated a brute-force attack against a Windows endpoint and successfully detected it using Wazuh.

## MITRE ATT&CK Mapping
- **Technique**: T1110.001 – Password Guessing
- **Tactic**: Credential Access

## Attack Simulation
- Multiple failed login attempts were generated against a local Windows account
- Used incorrect passwords repeatedly within a short time window

## Detection Details
| Field                  | Value                          |
|------------------------|--------------------------------|
| Rule ID                | 60122 (or related authentication failure rules) |
| Event ID               | 4625 (Failed Logon)            |
| Severity               | Medium                         |
| Source                 | Windows Security Event Log     |

## Investigation Steps
1. Alert triggered in Wazuh Dashboard
2. Reviewed the full event details (username, source IP, logon type)
3. Correlated multiple failed attempts within a short time period
4. Confirmed it matched brute-force behavior

## Evidence
- Multiple Event ID 4625 logs
- Screenshot of the alert in Wazuh Dashboard (see `screenshots/` folder)

## Response / Recommendations
- Account lockout policy should be enforced
- Monitor for repeated failed logons from the same source
- Consider implementing multi-factor authentication where possible

## Status
✅ Successfully detected and documented.
