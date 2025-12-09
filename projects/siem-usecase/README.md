# 🛡️ SIEM & Detection Engineering (Wazuh)

### **1. 🚀 Executive Summary**

This project established a functional **Security Information and Event Management (SIEM)** environment using **Wazuh** and the **Elastic Stack (Kibana)**. The goal was to move beyond simple logging to implement **proactive detection engineering** capabilities. I successfully built the core infrastructure, onboarded endpoints, and developed **custom, high-fidelity detection rules** to identify specific threat activities, significantly improving alert quality and operational visibility.



---

### **2. 🛠️ Technical Implementation**

| Component | Role in Project | Demonstrated Skill |
| :--- | :--- | :--- |
| **Wazuh Manager** | Centralized analysis, correlation, and rule processing. | **SIEM Deployment & Configuration** |
| **Wazuh Agents** | Installed on Windows and Linux endpoints. | **Endpoint Onboarding & Management** |
| **Elastic Stack (Kibana)** | Used for data visualization, dashboard creation, and alert triage. | **Data Visualization & Log Aggregation** |

#### **Detection Engineering Focus**

* **Custom Rules:** Developed rules using Wazuh Decoders and Rulesets to detect unauthorized execution and privilege escalation attempts not covered by default configurations.
* **Tuning:** Fine-tuned existing rules to minimize **False Positives (FPs)**, ensuring the SOC team only sees actionable alerts.
* **Dashboard Creation:** Built a dedicated Kibana dashboard for L1/L2 analysts, allowing them to rapidly **triage, prioritize, and investigate** alerts based on threat score and MITRE ATT&CK ID.

---

### **3. 📈 Key Outcomes**

* **Mitre ATT&CK Coverage:** Successfully implemented rules to detect techniques like **PowerShell abuse (T1059)** and **service creation (T1543)**.
* **Alert Fidelity:** Proof of ability to create **high-fidelity alerts** that deliver actionable intelligence for threat hunting.
* **Evidence:**
    * [Link to Custom Rule YML Files on GitHub]
