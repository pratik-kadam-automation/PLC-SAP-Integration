<img width="1536" height="1024" alt="file_00000000296871faac28cb23b635b555" src="https://github.com/user-attachments/assets/74e61b93-a913-439d-9c26-e7ffb43ecd07" />

# PLC–SAP Integration (RP2B)

## 📌 Overview
This repository demonstrates a real-world industrial integration where production data is collected from a PLC and prepared for SAP ingestion using a reliable, file-based handshake mechanism.

The solution is designed for shop-floor environments where robustness, traceability, and controlled data transfer are critical.

---

## 🏭 System Architecture (High Level)

PLC → Ethernet → Data Collection Service → File Validation → SAP Pickup

- PLC acts as the source of truth
- Data is captured only at **production cycle completion**
- SAP reads validated files from a predefined directory

---

## 📟 PLC Data Mapping (Sanitized)

| Parameter        | PLC Address        | Description                         |
|------------------|--------------------|-------------------------------------|
| Total Weight     | DB100.DBW118       | Accumulated production weight       |
| Line Speed       | DB100.DBW18        | Current process speed               |
| Cycle Trigger    | DI 1.0             | Signals end of production cycle     |

> ⚠️ Note: Addresses shown are for demonstration purposes only.

---

## 📁 Folder Design & Purpose

| Folder | Description |
|------|-------------|
| `Error/` | Created when PLC communication fails or data validation errors occur |
| `TXT/` | Production data files generated at cycle end (SAP pickup location) |
| `SVC/` | Historical archive for traceability and audit |

---

## 🔁 Data Flow Logic

1. PLC process runs normally
2. DI 1.0 becomes TRUE → cycle completed
3. PLC values are read via Ethernet
4. Data is validated (range, communication status)
5. TXT file is generated
6. SAP system picks up the file
7. Copy is stored in SVC for history

This approach avoids:
- Duplicate SAP entries
- Partial or corrupt data uploads
- Manual operator dependency

---

## 🛠️ Technology Stack

- PLC: Siemens (S7 family – generic)
- Communication: Industrial Ethernet
- Integration Logic: VB.NET (sample structure)
- SAP Interface: File-based ingestion
- OS: Windows Industrial PC

---

## 🎯 Why This Design

✔ Simple & robust  
✔ Easy to audit  
✔ Works without OPC dependency  
✔ Industry-proven approach  
✔ Scalable to MQTT / OPC UA later  

---

## 🔒 Security & IP Protection

- No real PLC IPs included
- No SAP credentials stored
- Company-specific logic removed
- Sample configs only

This repository is intended for **learning, portfolio, and architectural reference**.

---

## 🚀 Future Enhancements

- MQTT-based real-time publishing
- Python data collector
- Central historian (InfluxDB)
- Dashboard (Grafana / Power BI)

---

## 📎 License
For educational and portfolio use only.

---

## 📬 Author
Pratik Kadam  
Industrial Automation | PLC | SAP | IoT 