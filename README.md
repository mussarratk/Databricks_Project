# Databricks_Project

# 🛒 ShopVista: End-to-End Azure Data Engineering: E-commerce Pipeline with Databricks & PySpark
   

## 📌 Project Overview

ShopVista is a simulated high-growth e-commerce platform that was constrained by scattered data, manual consolidation, and delayed reporting cycles.

This project solves these bottlenecks by delivering a **centralized, scalable, and fully automated data platform** on Microsoft Azure. By utilizing Azure Databricks, Unity Catalog, and a strict Medallion Architecture, raw operational data is transformed into high-performance, analytics-ready datasets that power an interactive Power BI dashboard for executive decision-making.

## 🎯 The Business Value

  * **Eliminated Manual Data Prep:** Replaced fragile, manual flat-file workflows with automated cloud pipelines.
  * **Accelerated Insights:** Reduced reporting turnaround from hours to minutes.
  * **Single Source of Truth:** Created a reliable, governed foundation for enterprise analytics.
  * **Self-Service BI:** Empowered business stakeholders to track KPIs in real-time.

-----

## 🏗️ Technical Architecture & Medallion Pipeline

The solution leverages an ELT approach, orchestrated on Azure:


<img width="1365" height="575" alt="image" src="https://github.com/user-attachments/assets/35ddf511-04c1-41f5-80f6-f0a280c83264" />


### 1\. Data Ingestion (Raw Zone)

  * **Storage:** Azure Data Lake Storage Gen2 (ADLS)
  * **Action:** Source CSV files (Orders, Customers, Products, etc.) land in dedicated ADLS directories, establishing a centralized and traceable data lake.

### 2\. Medallion Architecture Processing (Databricks)

Using PySpark and Delta Lake, data progresses through three strict refinement layers:

| Layer | Purpose | Key Transformations & Enforcements |
| :--- | :--- | :--- |
| **🥉 Bronze** | Raw Ingestion | Minimal transformation, historical storage, and strict schema enforcement. |
| **🥈 Silver** | Cleansing & Conforming | Deduplication, handling nulls/invalid records, referential integrity checks, and standardization. |
| **🥇 Gold** | Business Intelligence | Star schema modeling (Fact & Dimension tables), aggregated metrics, optimized for Power BI. |

### 3\. Automated Orchestration

To ensure data freshness while optimizing compute costs, processing is divided into scheduled Databricks Jobs:

  * **🔁 Daily Refresh:** Processes Dimension tables (Customers, Products, Categories, Brands, Date) and `Fact_Order_Items`. Dependencies are strictly enforced to guarantee referential consistency.
  * **📅 Monthly Refresh:** Processes heavy historical loads, specifically `Fact_Order_Returns` and `Fact_Order_Shipments`, enabling long-term trend analysis.

-----

## 📊 Analytics & Dashboards

`[Insert Dashboard Preview Image Here]` | [🔗 View Live Dashboard](https://www.google.com/search?q=Link-to-dashboard)

The Gold layer directly feeds a Power BI data model, delivering actionable insights on:

  * **Revenue & Growth:** Total Sales, Units Sold, and Monthly Revenue Trends.
  * **Customer Behavior:** Repeat Customer Rates and Distribution by Region.
  * **Product Performance:** Sales split by Brand, Category, and Channel (Mobile vs. Website).

-----

## 🧠 Developer Profile & Highlighted Skills

I am a **Databricks Certified Associate** currently pursuing an MBA in Data Science. With over 4 years of experience driving high-stakes E-commerce operations for global brands, I am deeply passionate about engineering the narrative—turning fragmented data into scalable data pipelines and enabling data-driven insights.

**Core Competencies Demonstrated in This Project:**

  * **Cloud Data Engineering:** Architecting end-to-end solutions using Microsoft Azure (ADLS) and understanding broader cloud concepts across AWS.
  * **Big Data Processing:** Heavy-duty ETL/ELT transformations using **Python, SQL, and PySpark** within Azure Databricks.
  * **Data Modeling:** Designing robust Medallion Architectures (Bronze, Silver, Gold) and Star Schemas for business analytics.
  * **Governance & Orchestration:** Utilizing Unity Catalog and automating complex workflows via Databricks Jobs.
  * **Business Intelligence:** Bridging the gap between raw data and executive strategy using Power BI.

-----

## 🙏 Acknowledgements

Special thanks to **Codebasics** for their exceptional Data Engineering Bootcamp, hands-on project guidance, and real-world problem statements that helped inspire the design and implementation of this end-to-end cloud platform.

---








---










---
Azure Workspace

<img width="1366" height="580" alt="image" src="https://github.com/user-attachments/assets/142bb989-0721-4f86-940f-4b07c9db942a" />
<img width="1278" height="362" alt="image" src="https://github.com/user-attachments/assets/9348cb62-6c42-4bd4-8717-7749fe1af7d1" />


<img width="1342" height="615" alt="image" src="https://github.com/user-attachments/assets/82f6e2db-1f34-4a3f-94a3-35d4351e48fc" />

<img width="1053" height="320" alt="image" src="https://github.com/user-attachments/assets/6617f038-89a8-4c68-bd11-7b32839e2695" />
<img width="1335" height="582" alt="image" src="https://github.com/user-attachments/assets/d08648c5-ff96-4d67-b16b-20d563136d57" />
<img width="471" height="405" alt="image" src="https://github.com/user-attachments/assets/7189b8a2-1999-4fec-9371-e6117061c252" />



<img width="1267" height="549" alt="image" src="https://github.com/user-attachments/assets/2d932c63-8942-4894-9099-a828e6d981a1" />
<img width="1038" height="491" alt="image" src="https://github.com/user-attachments/assets/1e3375dc-a0e6-48aa-89de-f3468f4d2013" />

Managed Location - uc-data container - contains managed table which will be saved in medallion layer
Raw Location - ecomm-raw-data container - contains raw files which is for external volume raw/landing to point to 
<img width="704" height="598" alt="image" src="https://github.com/user-attachments/assets/e70168db-2270-4a37-ac37-71e7d82ef61c" />

Connection - Created 2 external location and 2 external credentials for 2 containers  
<img width="1346" height="440" alt="image" src="https://github.com/user-attachments/assets/aa6db235-b313-418d-9e58-abeb8527bc19" />

<img width="1180" height="485" alt="image" src="https://github.com/user-attachments/assets/f9cd7916-faa9-4f57-bdd5-9bddaab3d8aa" />
<img width="1356" height="615" alt="image" src="https://github.com/user-attachments/assets/4e466a28-23d2-4e90-a5f5-ef0f52182c67" />

databricks - through Access Connector : got data into databricks

<img width="1328" height="585" alt="image" src="https://github.com/user-attachments/assets/8ebe0123-b295-4679-99e4-8d31074de85c" />
<img width="1349" height="633" alt="image" src="https://github.com/user-attachments/assets/8fb5ee05-7118-4634-938f-ce84d3e47d37" />

/Volumes/ecommerce/raw/raw_landing - external volume
<img width="1341" height="525" alt="image" src="https://github.com/user-attachments/assets/b13b0c9e-3d0f-416e-a983-b85bd5a5fd38" />

Through that raw connection - ingested data in bronze layer - and only dimension tables





---

