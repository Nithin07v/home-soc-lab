# 🛡️ Splunk SOC Home Lab

> A hands-on Security Operations Center (SOC) Home Lab built to simulate real-world security monitoring using Splunk Enterprise, Sysmon, Windows 11, Ubuntu Server, and Kali Linux.

---

## 📖 Project Overview

This project documents my journey of building a SOC Home Lab from scratch to gain practical experience in Security Information and Event Management (SIEM), Windows logging, and threat detection.

The lab is designed to simulate a real SOC environment where Windows security events are collected, forwarded, indexed, and analyzed using Splunk Enterprise.

Rather than only studying cybersecurity concepts, this project focuses on implementing and troubleshooting real technologies commonly used by security analysts.

---

# 🏗️ Lab Architecture

```text
                     Kali Linux
                 (Attack Simulation)
                         │
                         ▼
                  Windows 11 VM
          ┌────────────────────────┐
          │ • Windows Event Logs   │
          │ • Sysmon               │
          │ • Splunk Forwarder     │
          └──────────┬─────────────┘
                     │
             TCP Port 9997
                     │
                     ▼
             Ubuntu 24.04 LTS
          Splunk Enterprise Server
                     │
                     ▼
          Search • Monitoring • Analysis
```

---

# 🎯 Objectives

This project aims to:

- Build a functional SOC Home Lab
- Deploy Splunk Enterprise on Ubuntu
- Configure centralized Windows log collection
- Install and configure Sysmon
- Forward Windows Event Logs using Splunk Universal Forwarder
- Learn Splunk Search Processing Language (SPL)
- Create a foundation for threat hunting and detection engineering

---

# 🖥️ Environment

| Component | Technology |
|-----------|------------|
| Hypervisor | VMware Workstation |
| SIEM | Splunk Enterprise |
| Log Forwarder | Splunk Universal Forwarder |
| Monitoring | Sysmon |
| Server | Ubuntu 24.04 LTS |
| Endpoint | Windows 11 |
| Attacker Machine | Kali Linux |

---

# ✅ Completed

- Installed Ubuntu 24.04
- Installed Splunk Enterprise
- Configured Splunk receiving port (9997)
- Installed Windows 11
- Installed Splunk Universal Forwarder
- Configured Windows Event Log forwarding
- Installed Sysmon
- Configured Sysmon logging
- Verified Windows logs in Splunk
- Verified Sysmon events in Splunk
- Troubleshot forwarding and Windows service permission issues

---

# 📊 Sample SPL Queries

### Show all indexed events

```spl
index=*
```

### Windows Security Events

```spl
source="WinEventLog:Security"
```

### Sysmon Events

```spl
source="WinEventLog:Microsoft-Windows-Sysmon/Operational"
```

### Process Creation

```spl
EventCode=1
```

### Failed Login Attempts

```spl
EventCode=4625
```

---

# 📷 Screenshots

![image alt](https://github.com/Nithin07v/home-soc-lab/blob/c685fc82274e7e633045c9ed8f86ad1f3bfd940a/Screenshot%202026-07-07%20214507.png)
![image alt](https://github.com/Nithin07v/home-soc-lab/blob/dd81f7bc89cad5364b707774b1ddb6ca370a9084/Screenshot%202026-07-07%20222238.png)


Suggested screenshots:

- VMware Virtual Machines
- Splunk Search Interface
- Sysmon Process Creation Events
- Windows Event Logs
- Universal Forwarder Configuration

---

# 🛠️ Challenges & Troubleshooting

During this project I encountered several real-world issues, including:

- Network connectivity between virtual machines
- Splunk Universal Forwarder configuration
- Windows Event Log forwarding
- Sysmon permission issues (`errorCode=5`)
- Service account configuration
- Verifying log ingestion using Splunk searches

Resolving these issues provided valuable hands-on troubleshooting experience.

---

# 📚 Skills Gained

- SIEM Deployment
- Splunk Administration
- Windows Event Logging
- Sysmon Configuration
- Log Collection
- Event Analysis
- Linux Administration
- VMware Networking
- Basic SPL
- Troubleshooting

---

# 🚀 Future Roadmap

The lab will continue to expand with additional security monitoring capabilities, including:

- Network scanning detection (Nmap)
- PowerShell detection
- Network connection monitoring
- Threat hunting
- Custom SPL detections
- Dashboards
- Alerts
- Detection engineering
- Simulated attack investigations
- Incident response scenarios

---

# 📈 Current Progress

| Phase | Status |
|--------|--------|
| Infrastructure Setup | ✅ Complete |
| Log Collection | ✅ Complete |
| Sysmon Integration | ✅ Complete |
| SPL Learning | 🟡 In Progress |
| Attack Simulation | ⏳ Planned |
| Threat Hunting | ⏳ Planned |
| Detection Engineering | ⏳ Planned |
| Dashboards & Alerts | ⏳ Planned |

---

# 💡 Key Takeaways

Building this lab has strengthened my understanding of:

- How Windows logs are generated
- How Sysmon enhances endpoint visibility
- How logs are forwarded to a SIEM
- Basic security event investigation
- Practical troubleshooting in a SOC environment

This project is continuously updated as I learn and implement new security concepts.

---

