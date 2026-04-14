# Volve Field: Production Analytics & Containerized Infrastructure

> **An end-to-end production analysis system for the Volve Field, featuring a containerized PostgreSQL backend and a Jupyter-based analytics dashboard orchestrated via Docker Compose.**

---

## Overview
This project demonstrates the transition from local data analysis to a **production-ready infrastructure**. Using the **Volve Open Dataset**, I built an automated pipeline that ingests production data into a relational database and visualizes key performance indicators (KPIs) through a dynamic dashboard.

### 🎯 Core Capabilities
* **Containerized Environment:** Orchestrated a multi-service architecture using **Docker Compose** to ensure environment parity.
* **Relational Data Modeling:** Established a persistent **PostgreSQL** database to store and query production logs efficiently.
* **Production KPI Analytics:** Analyzed daily oil, gas, and water production rates to identify field life-cycle trends.
* **Interactive Visualization:** Developed a comprehensive dashboard to monitor well performance and production efficiency.

---

## Infrastructure Architecture (Docker)
The system is built on a custom bridge network containing two primary services:

1. **Jupyter Analytics Service:** A pre-configured Data Science environment (`jupyter/datascience-notebook`) mapped to local volumes for persistent analysis.
2. **PostgreSQL Production DB:** A persistent database container used for storing structured production data, secured with custom environment credentials.

---

## Production Performance Dashboard
The analytical core of this project is an interactive dashboard that translates raw PostgreSQL data into field-level insights.
![Volve Production Dashboard](/volve_dashboard.png)
### 📈 Key Performance Indicators (KPIs)
* **Daily Production Volume:** Real-time tracking of Oil (bbl/d), Gas (MSCF/d), and Water (bbl/d) rates.
* **Wellhead Pressure Trends:** Correlation analysis between choke sizes and wellhead pressure to optimize flow.
* **Water Cut Analysis:** Monitoring the ratio of water to total fluids to predict reservoir depletion phases.
* **Cumulative Field Recovery:** A macro-view of the total volume extracted versus estimated ultimate recovery (EUR).
