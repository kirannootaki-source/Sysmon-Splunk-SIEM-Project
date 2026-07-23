# Project Architecture

## Overview

This document describes the architecture of the Windows endpoint monitoring environment implemented in this project. The solution leverages **Sysmon**, **Splunk Universal Forwarder**, and **Splunk Enterprise** to collect, forward, index, and visualize security events for threat monitoring and analysis.

---

## Architecture Diagram

```
+----------------------+
|  Windows 11 Endpoint |
+----------+-----------+
           |
           | Generates Security Events
           v
+----------------------+
|        Sysmon        |
| (Windows Event Logs) |
+----------+-----------+
           |
           | Collects Events
           v
+-------------------------------+
| Splunk Universal Forwarder    |
+---------------+---------------+
                |
                | Forwards Logs (TCP 9997)
                v
+-------------------------------+
|      Splunk Enterprise        |
|      Indexing & Searching     |
+---------------+---------------+
                |
                | SPL Searches
                v
+-------------------------------+
| Security Dashboards & Reports |
+-------------------------------+
```

---

## Components

### Windows Endpoint

The Windows 11 endpoint acts as the monitored system where security events are generated through normal system and user activity.

---

### Sysmon

Sysmon extends native Windows logging by generating detailed security events including:

- Process Creation
- Network Connections
- File Creation
- Registry Modifications
- DNS Queries

---

### Splunk Universal Forwarder

The Splunk Universal Forwarder collects Sysmon Operational logs from the Windows Event Log and securely forwards them to the Splunk Enterprise server.

Configuration files:

- `inputs.conf`
- `outputs.conf`

---

### Splunk Enterprise

Splunk Enterprise receives, indexes, and stores Sysmon logs for security analysis.

It provides:

- Event Searching
- Log Correlation
- Dashboard Visualization
- Threat Investigation

---

## Data Flow

1. Windows generates system activity.
2. Sysmon captures detailed security events.
3. Splunk Universal Forwarder collects Sysmon logs.
4. Logs are forwarded to Splunk Enterprise.
5. Splunk indexes and stores events.
6. SPL queries analyze the collected data.
7. Dashboards visualize security events for monitoring.

---

## Security Events Monitored

| Event ID | Description |
|----------|-------------|
| 1 | Process Creation |
| 3 | Network Connection |
| 11 | File Creation |
| 13 | Registry Modification |
| 22 | DNS Query |

---

## Dashboards

The following dashboards were developed as part of this project:

- Sysmon Monitoring Dashboard
- Top 10 Executed Processes
- Top Users Creating Processes
- Total Process Creation Events
- Network Connections Dashboard
- DNS Queries Dashboard

---

## Outcome

This architecture provides centralized visibility into Windows endpoint activity by integrating Sysmon with Splunk Enterprise. The collected telemetry enables efficient monitoring, event investigation, and supports entry-level SOC operations and security analysis.
