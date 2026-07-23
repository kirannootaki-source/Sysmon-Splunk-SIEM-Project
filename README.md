# 🛡️ Sysmon + Splunk SIEM Project

## 📌 Project Overview

This project demonstrates how to monitor Windows endpoint activity using **Sysmon**, **Splunk Enterprise**, and **Splunk Universal Forwarder**. Sysmon generates detailed Windows event logs, which are forwarded to Splunk for centralized monitoring, searching, and dashboard visualization.

The project showcases practical SIEM skills used by SOC Analysts to detect suspicious activities on Windows endpoints.

---

## 🎯 Objectives

- Monitor Windows endpoint activity using Sysmon
- Collect Sysmon logs in Splunk Enterprise
- Analyze security events using SPL queries
- Build dashboards for security monitoring
- Gain hands-on experience with SIEM technologies

---

## 🛠️ Technologies Used

- Splunk Enterprise
- Splunk Universal Forwarder
- Sysmon
- Windows 11
- SPL (Search Processing Language)

---

## 📂 Project Structure

```
Sysmon-Splunk-SIEM-Project
│
├── screenshots/
├── configs/
│   ├── inputs.conf
│   ├── outputs.conf
│   └── sysmonconfig.xml
│
├── queries/
│   └── spl_queries.md
│
├── docs/
│
└── README.md
```

---

## 🔍 Sysmon Event IDs Used

| Event ID | Description |
|----------|-------------|
| 1 | Process Creation |
| 3 | Network Connection |
| 11 | File Creation |
| 13 | Registry Event |
| 22 | DNS Query |

---

## 📊 Dashboards Created

- Sysmon Monitoring Dashboard
- Top 10 Executed Processes
- Top Users Creating Processes
- Total Process Creation Events
- Network Connections Dashboard
- DNS Queries Dashboard

---

## 📸 Project Screenshots

All screenshots are available in the **screenshots** folder.

They include:

- Sysmon Installation
- Event Viewer Logs
- Splunk Universal Forwarder Configuration
- Receiving Port Configuration
- SPL Search Results
- Dashboard Visualizations

---

## 📝 SPL Queries

The SPL queries used in this project are available in:

```
queries/spl_queries.md
```

---

## ⚙️ Configuration Files

Configuration files are available in the **configs** folder.

- inputs.conf
- outputs.conf
- sysmonconfig.xml

---

## 💡 Skills Demonstrated

- SIEM Monitoring
- Log Analysis
- Windows Event Monitoring
- Threat Detection
- Splunk Enterprise Administration
- Splunk Universal Forwarder Configuration
- Dashboard Development
- Search Processing Language (SPL)

---

## 🚀 Future Improvements

- Email Alerting
- Real-Time Monitoring
- Correlation Searches
- Custom Detection Rules
- MITRE ATT&CK Mapping

---

## 👨‍💻 Author

**Sai Kiran**

Cybersecurity Enthusiast | SOC Analyst Aspirant

---

⭐ If you found this project useful, feel free to star this repository.
