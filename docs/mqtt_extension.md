# MQTT Extension – Future Architecture

## Purpose
Enable real-time analytics and dashboards without impacting
existing PLC–SAP integration.

## Extended Flow

PLC -> IPC Application
IPC Application -> MQTT Broker
MQTT Broker -> Subscribers

Subscribers may include:
- Dashboards
- Historian (InfluxDB)
- Alert services
- Cloud analytics

## Design Principles
- SAP integration remains file-based
- MQTT operates in parallel
- PLC load is unchanged
- Failure of MQTT does not affect SAP

## Benefits
- Industry 4.0 readiness
- Scalable data consumers
- Real-time visibility
