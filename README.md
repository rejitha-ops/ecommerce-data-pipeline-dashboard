# 📊 End-to-End Enterprise E-Commerce Data Pipeline
### Technology Stack: Python (Pandas, SQLAlchemy, PyMySQL), MySQL Server, Power BI Desktop

---

## 🎯 Project Objective
The goal of this project is to simulate an enterprise-level data analyst workflow by building a complete, high-speed data pipeline. Using a relational database of over 100,000 transaction records, this project extracts raw data, performs structural text casing and date cleaning using Python, injects the tables into a local MySQL database engine, and constructs an optimized, interactive executive dashboard in Power BI.

---

## 🏗️ Data Architecture Flow
## 🛠️ Step-by-Step Implementation Breakdown

### 🐍 Phase 1: Python ETL & Exploratory Data Analysis (EDA)
Using **Python IDLE** with `pandas`, the raw multi-table datasets were processed to resolve underlying data quality and structural challenges:
* **Localization Mapping:** Automatically matched a secondary translation schema to convert over 70 distinct product category keys from Portuguese to English, maintaining reporting readability.
* **Feature Engineering:** Calculated explicit operational operational metrics including total transaction values (`price + freight_value`) and exact delivery durations.
* **Data Profiling Audit:** Conducted missing-value scans and verified data integrity by screening for duplicate rows across 100,000+ entries.
* **High-Speed Database Connection:** Utilized `sqlalchemy` and `pymysql` drivers to establish a direct local connection, pushing prepped files into a relational SQL engine in under 5 seconds.

### 🗄️ Phase 2: MySQL Database Architecture & Analysis
Data tables were staged into **MySQL Workbench** to run analytical scripts. Six comprehensive business queries were engineered to capture operational, financial, and marketing performance:
1. **Top Product Performance:** Identified `Health & Beauty` as the organization's primary monetization channel, generating over **$1.23M in revenue** across 9,465 items sold.
2. **Logistics Delay Breakdown:** Utilized calendar functions (`DATEDIFF`) to identify regional shipping bottlenecks, exposing that northern states like Roraima (RR) average prolonged transit times of **29.3 days**.
3. **Fulfillment Performance Proportions:** Modeled delivery metrics using `CASE WHEN` tracking parameters, confirming an **91.89% On-Time / Early rate** (88,644 orders) against an **8.11% delay rate** (7,826 orders).
4. **Geographic Average Order Value (AOV):** Calculated financial values per customer ticket by state, isolating high-value customer locations.

### 🎨 Phase 3: Power BI Data Modeling & Dashboards
Cleaned tables were loaded live into **Power BI Desktop** to establish a clean reporting environment:
* **Star Schema Architecture:** Constructed an optimized data model by mapping strict 1-to-many (`1:*`) directional filtering relationships between central fact tables and descriptive dimension tables (`customers`, `products`).
* **Temporal Tracking Optimization:** Converted text metrics into active `Date/Time` formatting to unlock automated **Date Hierarchies**, displaying clear timelines without text overlap.
* **Interactive Dynamic Slicers:** Deployed interactive filtering components allowing end-users to query specific customer states and timeline date windows on the fly.

---
## 📊 Final Executive Dashboard Performance Metrics
* **Total Revenue Generated:** $13.59M
* **Total Completed Transactions:** 98.67K Orders
* **Average Order Value (AOV):** $120.65 per checkout
* **Operational On-Time Delivery Rate:** 91.89%
