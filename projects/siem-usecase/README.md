# SIEM Use Case Implementation (Wazuh)

## 📌 Project Overview
This project demonstrates hands-on SOC skills by configuring **Wazuh SIEM**, onboarding endpoints, creating **custom detection rules**, and analyzing logs for brute-force attacks, privilege escalation, and suspicious PowerShell execution.

## 🎯 Objectives
- Deploy Wazuh SIEM (Manager + Agent)
- Ingest Windows/Linux logs
- Create detection rules & alerts
- Build dashboards
- Map detections to MITRE ATT&CK

---

## 🛠 Tools & Technologies
- Wazuh SIEM (Open Source)
- Windows 10 endpoint (Sysmon optional)
- Ubuntu/Kali Linux endpoint
- VirtualBox / VMware
- Log collection modules (Winlogbeat/Filebeat)

---

## ⚙️ Step-by-Step Implementation

### **1️⃣ Install Wazuh Manager (Linux VM)**
```bash
curl -s https://packages.wazuh.com/4.7/wazuh-install.sh | bash
