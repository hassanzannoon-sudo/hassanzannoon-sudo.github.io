# 🌐 Network Intrusion Analysis (Suricata/Nmap)

### **1. 🚀 Executive Summary**

This project focused on the **Network Detection** component of a defensive strategy. I successfully simulated common reconnaissance and attack attempts against a target network and used a Network Intrusion Detection System (NIDS), **Suricata**, to monitor, capture, and alert on the malicious traffic. The output demonstrated proficiency in **packet analysis** and the ability to extract **actionable Indicators of Compromise (IOCs)**.



---

### **2. 🛠️ Technical Implementation**

| Component | Role in Project | Demonstrated Skill |
| :--- | :--- | :--- |
| **Kali Linux / Nmap** | Used to simulate reconnaissance (port scans) and brute-force attacks against a target system. | **Attack Simulation & Offensive Testing** |
| **Suricata (NIDS)** | Deployed to monitor network traffic (IDS mode). Configured with appropriate rule sets (ET Open). | **Network Monitoring & Rule-Based Detection** |
| **Wireshark / PCAP** | Used to analyze the raw network traffic captured by the NIDS. | **Packet Analysis & Protocol Interpretation** |

#### **Simulation and Analysis Steps**

1.  **Preparation:** Configured Suricata to capture traffic on the simulated network segment.
2.  **Simulation:** Executed various attacks, including **TCP SYN Scans** (stealthy reconnaissance) and failed **HTTP Brute-Force** attempts.
3.  **Alerting:** Reviewed the generated Suricata alerts (`fast.log`) to confirm detection.
4.  **Verification:** Used **Wireshark** to analyze the corresponding **PCAP (Packet Capture)** files, verifying the source and nature of the traffic that triggered the alerts.

---

### **3. 📈 Key Outcomes**

* **Alert Generation:** Confirmed that both reconnaissance and intrusion attempts triggered high-severity Suricata alerts.
* **IOC Extraction:** Successfully extracted and analyzed the following **Indicators of Compromise (IOCs)** from the alerts and PCAP:
    * Malicious **Source IP** and **Destination IP**
    * Target **Port** and **Protocol**
    * Specific **Suricata Signature ID** used for detection
* **Evidence:**
    * [Link to Nmap Scan Commands / Suricata Configuration on GitHub]
