# Data Lifecycle – Production to SAP

## Stage 1: Data Generation
- PLC sensors generate raw values
- Values continuously update in PLC memory

## Stage 2: Trigger
- Digital Input indicates cycle completion
- Data becomes valid only at this point

## Stage 3: Collection
- IPC reads PLC values over Ethernet
- Snapshot-based data capture

## Stage 4: Validation
- Communication check
- Range validation
- Completeness verification

## Stage 5: Distribution
- Valid data -> TXT folder (SAP pickup)
- Invalid data -> Error folder

## Stage 6: Persistence
- Successful data archived in SVC folder
- Supports audit and traceability

## Stage 7: Consumption
- SAP processes TXT file
- No direct PLC dependency
