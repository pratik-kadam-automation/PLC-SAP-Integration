# Sequence Diagram – PLC to SAP Integration

## Normal Operation Flow

PLC -> IPC Application : Production running
PLC -> IPC Application : Cycle Complete (DI = TRUE)

IPC Application -> PLC : Read Total Weight
IPC Application -> PLC : Read Line Speed

IPC Application -> IPC Application : Validate data
IPC Application -> TXT Folder : Write production file

TXT Folder -> SAP : File pickup
IPC Application -> SVC Folder : Archive history copy

Note:
- One cycle generates exactly one SAP entry
- No duplicate uploads
- No retry storm
