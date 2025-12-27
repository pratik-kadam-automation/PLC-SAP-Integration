<img width="1536" height="1024" alt="file_00000000296871faac28cb23b635b555" src="https://github.com/user-attachments/assets/74e61b93-a913-439d-9c26-e7ffb43ecd07" />
# PLC-SAP-Integration
PLC data collection and SAP integration using VB.NET
# PLC-SAP Integration

# PLC-SAP Integration

### 📌 Overview
This project demonstrates a real-world integration between industrial PLC systems and SAP for automated production data transfer.  
It uses a file-based handshake method to reliably push PLC variables into SAP while minimizing manual data entry.

---

## 🚀 Key Features
✅ Collects PLC data over Ethernet  
✅ Writes production cycle data into structured TXT files  
✅ Logs historical data for analysis  
✅ Handles error conditions when communication fails

---

## 🧠 How It Works

### 📁 Folder Structure
| Folder | Purpose |
|--------|---------|
| `Error/` | Files generated when PLC communication fails |
| `TXT/` | Data files created at the end of each production cycle |
| `SVC/` | Historical data archive |

### 📟 PLC Variables
| Variable | PLC Reference | Description |
|----------|---------------|-------------|
| Total Weight | `DB100.DBW118` | Accumulated weight |
| Line Speed | `DB100.DBW18` | Current line speed |
| Process Sensor | `DI 1.0` | Trigger for cycle end |

---

## 🛠️ Technologies Used
- **VB.NET** for integration logic  
- **Ethernet communication** with PLC  
- File-based data generation (TXT / JSON)

---

## 🎯 Purpose
This solution:
- Removes manual SAP data entry
- Improves reliability and traceability
- Prepares factory data for digital transformation

---

## 📌 How to Use (Example)
1. Clone the repository  
2. Update `config_sample.json` with your PLC and folder paths  
3. Build and deploy with VB.NET  
4. PLC pushes data at cycle end → TXT file generates → SAP picks it up

---

## 🧪 Notes
❗ This is a **sample integration structure**. Replace sample config values before deployment.  
❗ Do not include real IPs or sensitive credentials in the GitHub repository.

---

## 📎 License
This project is for educational and portfolio purposes.

---

## 📬 Contact
If you want help adapting this integration to your environment, feel free to reach out!