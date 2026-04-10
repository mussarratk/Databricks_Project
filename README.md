# Databricks_Project

# 🛒 ShopVista: End-to-End E-Commerce Data Platform

   

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

`[Insert Architecture Diagram Here]`
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
