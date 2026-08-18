# Logging and Discover

## Core Concept

Wazuh does not store every raw log by default. Instead:

1. Agents collect logs
2. **Decoders** parse the logs and extract fields
3. **Rules** decide whether an event becomes an alert
4. Only matching events appear as alerts in the dashboard

## Discover Page

The **Discover** interface allows searching through indexed alerts.

### Useful Features

- Index pattern selector
- Search query (KQL / Lucene style)
- Time range selector
- Field list and event details

### Example Searches Practiced

- SSH authentication events: `decoder.name: sshd`
- Windows Defender detections: `data.win.system.eventID: 1116`
- Filtering by agent name and rule level

## Logs vs Rules vs Alerts

| Concept     | Description                              |
|-------------|------------------------------------------|
| Raw Logs    | Original events collected from agents    |
| Decoders    | Parse raw logs and extract fields        |
| Rules       | Decide if an event should generate an alert |
| Alerts      | Events that match rules and appear in the dashboard |

## Takeaway

Understanding the flow from raw logs → decoders → rules → alerts is fundamental to using Wazuh effectively as a SIEM.
