# Building Management System (BMS) Project

## 1. Project Overview
The BMS project is designed to monitor and control building environments (temperature, humidity, lighting, etc.) using an end-to-end data pipeline.  
It collects real-time sensor data, processes it using Apache Spark, stores and streams with Pinot DB, and visualizes insights in Apache Superset dashboards.

---

## 2. Project Planning

### Objectives
- Collect and process real-time environmental data from multiple buildings.
- Store, clean, and transform data for analysis.
- Build dashboards for energy efficiency and anomaly detection.
- Provide scalable architecture using open-source tools.

### Scope
- Includes: Data collection, processing, storage, modeling, and visualization.
- Excludes: Physical sensor installation or building control hardware.

### Deliverables
- Python data generator for simulation.
- Kafka topic for streaming.
- Spark Structured Streaming jobs.
- Trino is the distributed SQL query engine.
- Pinot DB
- Superset dashboards.


### Timeline (Example)

| Phase   | Task                          | Responsible    |
|---------|-------------------------------|----------------|
| Phase 1 | Data generator & Kafka setup  | Developer      |
| Phase 2 | Spark streaming pipeline      | Data Engineer  |
| Phase 3 | Pinot DB                      | Data Engineer  |
| Phase 4 | trino SQL engine              | Data Engineer  |
| Phase 5 | Superset dashboards           | Data Analyst   |


### Tools and Technologies
- **Languages:** Python, SQL  
- **Frameworks:** Spark, Pinot, Superset  
- **Streaming:** Kafka  
- **Storage:** Pinot
- **Visualization:** Apache Superset  
- **Version Control:** GitHub  

### Data Pipeline (Architecture)

- Python Generator  
  ↓  
- Kafka Topic (raw stream)  
  ↓  
- Spark Structured Streaming (processing)  
  ↓  
- Kafka new topic
  ↓  
- Pinot real-time DB 
  ↓   
- Trino SQL engine 
  ↓  
- Superset (visualization)  
  ↓  
- Dashboard (final output)




---

## 3. Stakeholder Analysis

### Stakeholder Identification

| Stakeholder | Role | Interest | Influence | Responsibility |
|--------------|------|-----------|-------------|----------------|
| Project Manager | Oversees project progress | High | High | Planning, coordination |
| Data Engineer | Builds data pipeline | High | High | Kafka, Spark, Hive setup |
| Data Analyst | Creates reports & dashboards | Medium | Medium | Visualization |
| Developer | Implements generator & controllers | High | Medium | Code development |
| Client / Building Owner | End-user of dashboard | High | Low | Provides requirements |
| IT Administrator | Manages deployment environment | Medium | High | Maintenance & scalability |

### Interest and Influence Matrix
- **High Interest & High Influence:** Project Manager, Data Engineer  
- **High Interest & Low Influence:** Client  
- **Low Interest & High Influence:** IT Administrator  
- **Low Interest & Low Influence:** General public or external observers  

---

## 4. References
- Apache Kafka Documentation  
- Apache Spark Structured Streaming Guide  
- Apache Superset Official Docs

## Note that
The project plan is flexible, and additional functionalities may be incorporated as development evolves.
