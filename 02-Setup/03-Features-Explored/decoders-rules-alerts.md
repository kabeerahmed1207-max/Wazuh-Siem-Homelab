# Decoders, Rules, and Alerts

## How Wazuh Processes Data

1. **Agent Configuration** → Defines what logs to collect
2. **Decoders** → Parse raw logs and extract fields
3. **Rules** → Match conditions and generate alerts (with severity level 1–15)
4. **Alerts** → Appear in the dashboard and can trigger notifications or Active Response

## Decoders

- Located under Server Management → Decoders
- Hundreds of built-in decoders for common log sources
- Example: Sysmon Event ID 1 decoder extracts Image, CommandLine, User, Hash, ParentImage, etc.

## Rules

- Located under Server Management → Rules
- Rules have levels from 1 (lowest) to 15 (highest criticality)
- Rules can be chained (`if_sid`, `if_group`)
- Example: Detect PowerShell execution via Sysmon

## Alerts

- Only events that match rules become alerts
- Can be filtered by rule level, agent, time range, etc.
- Can trigger notifications (email, Slack, etc.) or Active Response

## Takeaway

The combination of **Decoders + Rules** is the core detection engine of Wazuh. Mastering this is essential for detection engineering and SOC work.
