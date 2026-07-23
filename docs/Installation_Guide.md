# Installation Guide

## Overview

This document outlines the installation and configuration steps required to deploy a Windows endpoint monitoring environment using **Sysmon**, **Splunk Enterprise**, and **Splunk Universal Forwarder**.

---

## Environment

| Component | Version |
|----------|---------|
| Operating System | Windows 11 |
| Splunk Enterprise | Latest Stable Release |
| Splunk Universal Forwarder | Latest Stable Release |
| Sysmon | Sysinternals Sysmon |

---

## Prerequisites

Before starting, ensure the following software is available:

- Windows 11
- Splunk Enterprise
- Splunk Universal Forwarder
- Sysmon
- Administrative privileges
- Internet connection for downloads

---

## Installation Procedure

### Step 1 – Install Splunk Enterprise

Install Splunk Enterprise and verify that the web interface is accessible.

---

### Step 2 – Install Splunk Universal Forwarder

Install the Universal Forwarder and configure it to communicate with the Splunk Enterprise server.

---

### Step 3 – Install Sysmon

Deploy Sysmon using the provided **sysmonconfig.xml** configuration file.

The configuration enables detailed logging for process creation, network connections, DNS queries, registry modifications, and file creation events.

---

### Step 4 – Configure Splunk Inputs

Configure **inputs.conf** to collect Windows Sysmon Operational logs.

---

### Step 5 – Configure Outputs

Configure **outputs.conf** to forward collected events to the Splunk Enterprise receiving port.

---

### Step 6 – Restart Services

Restart the Splunk Universal Forwarder service to apply configuration changes.

---

### Step 7 – Validate Data Collection

Verify successful event ingestion by running SPL searches within Splunk Enterprise.

---

## Verification

Successful deployment should display the following Sysmon event types:

- Process Creation (Event ID 1)
- Network Connections (Event ID 3)
- File Creation (Event ID 11)
- Registry Events (Event ID 13)
- DNS Queries (Event ID 22)

---

## Configuration Files

The following configuration files are included in this repository:

- `inputs.conf`
- `outputs.conf`
- `sysmonconfig.xml`

---

## Result

Upon successful installation and configuration, Windows endpoint events are continuously collected, forwarded, indexed, and visualized through Splunk dashboards for security monitoring and threat detection.
