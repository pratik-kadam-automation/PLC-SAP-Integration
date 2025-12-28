Data Flow Description
PLC process runs normally
Digital input (cycle trigger) turns TRUE
PLC data is read via Ethernet
Data validation checks are performed
TXT file is generated
SAP picks up the file
Copy is stored in history folder
This flow ensures:

One SAP entry per production cycle
No partial uploads
Full audit trail