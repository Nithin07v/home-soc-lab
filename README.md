# 🛡️ Splunk SOC Home Lab

## 📌 Overview

This project demonstrates the creation of a Security Operations Center (SOC) Home Lab using Splunk Enterprise, Sysmon, Windows 11, Ubuntu Server, and Kali Linux.

The objective of this lab is to simulate a real SOC environment where security events are collected, forwarded, indexed, and analyzed using Splunk.

---

# 🏗️ Lab Architecture

```
                    Kali Linux
                  (Attacker VM)
                         │
                         │ Attack Simulation
                         ▼
                Windows 11 VM
         ┌──────────────────────────┐
         │ • Windows Event Logs     │
         │ • Sysmon                 │
         │ • Universal Forwarder    │
         └──────────────┬───────────┘
                        │
                        │ Port 9997
                        ▼
               Ubuntu 24.04 LTS
             Splunk Enterprise Server
                        │
                        ▼
                 Search & Monitoring
```

---

# 🎯 Project Objectives

- Build a functional SOC Home Lab
- Configure centralized log collection
- Forward Windows Event Logs to Splunk
- Install and configure Sysmon
- Collect security telemetry
- Learn basic Splunk Search Processing Language (SPL)
- Prepare the lab for attack simulation and threat hunting

---

# 🖥️ Technologies Used

- Splunk Enterprise
- Splunk Universal Forwarder
- Sysmon
- Ubuntu 24.04 LTS
- Windows 11
- Kali Linux
- VMware Workstation

---

# ⚙️ Configuration Completed

- Ubuntu Splunk Enterprise installation
- Receiving port (9997) enabled
- Windows Universal Forwarder installation
- Windows Event Log forwarding
- Sysmon installation
- Sysmon log forwarding
- Windows Event Viewer integration
- Log verification in Splunk

---

# 📊 Sample SPL Searches

### Show all events

```spl
index=*
```

### View Windows Security Logs

```spl
source="WinEventLog:Security"
```

### View Sysmon Events

```spl
source="WinEventLog:Microsoft-Windows-Sysmon/Operational"
```

### Process Creation

```spl
EventCode=1
```

### Failed Logins

```spl
EventCode=4625
```

---

# 📷 Screenshots

(Add screenshots here)

Examples:

- Splunk Dashboard
- Sysmon Event Logs
- VMware Virtual Machines
- Windows Forwarder Configuration
- Successful Sysmon Search

---

# 🧠 Skills Demonstrated

- SIEM Deployment
- Splunk Administration
- Windows Event Logging
- Sysmon Configuration
- Log Collection
- Security Monitoring
- Troubleshooting
- Linux Administration
- Basic SPL Queries

---

# 🚀 Future Improvements

- Attack simulation using Kali Linux
- Nmap detection
- PowerShell detection
- Threat hunting
- Dashboards
- Alerts
- Detection engineering
- Incident response scenarios

---

# 📚 Learning Outcomes

During this project I learned how to:

- Configure Splunk Enterprise
- Deploy Universal Forwarder
- Install and configure Sysmon
- Collect and analyze Windows Event Logs
- Troubleshoot log forwarding issues
- Search security events using SPL
- Build a basic SOC monitoring environment

---

## 👨‍💻 Author

**Nithin Vivek**

Aspiring Cybersecurity & SOC Analyst

LinkedIn: *(Add your profile)*

GitHub: *(Add your profile)*
