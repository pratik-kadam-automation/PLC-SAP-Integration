# PLC to SAP Flow

PLC communicates production data to an Industrial PC over Ethernet.

The IPC application:
- Reads PLC values
- Validates cycle completion
- Writes structured TXT files

SAP consumes only validated files.
Error and historical data are handled separately for reliability.