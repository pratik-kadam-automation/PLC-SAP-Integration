# Data Flow Description

1. PLC process runs normally
2. Digital input (cycle trigger) turns TRUE
3. PLC data is read via Ethernet
4. Data validation checks are performed
5. TXT file is generated
6. SAP picks up the file
7. Copy is stored in history folder

This flow ensures:
- One SAP entry per production cycle
- No partial uploads
- Full audit trail
