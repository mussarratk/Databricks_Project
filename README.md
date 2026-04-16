# Databricks_Project

# 🛒 ShopVista: End-to-End Azure Data Engineering: E-commerce Pipeline with Databricks & PySpark
   

## 📌 Project Overview

ShopVista is a rapidly growing e-commerce platform that faced major challenges due to data being scattered across multiple source systems and flat files. Business teams relied on manual data consolidation and static reports, resulting in delayed insights and limited visibility into sales, customers, and operations.

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

<img width="1357" height="637" alt="image" src="https://github.com/user-attachments/assets/2a961b2c-fd63-4998-96f6-1a4e5c203c76" />
<img width="666" height="601" alt="image" src="https://github.com/user-attachments/assets/7394890d-4153-4c9e-9a4c-3642ce8609cf" />
<img width="1348" height="627" alt="image" src="https://github.com/user-attachments/assets/3fc158fe-8fa3-416c-b113-5e03e92b5086" />

### 3\. Automated Orchestration

To ensure data freshness while optimizing compute costs, processing is divided into scheduled Databricks Jobs:

  * **🔁 Daily Refresh:** Processes Dimension tables (Customers, Products, Categories, Brands, Date) and `Fact_Order_Items`. Dependencies are strictly enforced to guarantee referential consistency.
  * **📅 Monthly Refresh:** Processes heavy historical loads, specifically `Fact_Order_Returns` and `Fact_Order_Shipments`, enabling long-term trend analysis.
  * 
<img width="1170" height="443" alt="image" src="https://github.com/user-attachments/assets/0c74d853-ece4-490b-8221-d57a7ef27a86" />
<img width="1012" height="568" alt="image" src="https://github.com/user-attachments/assets/1296c67f-2d5f-4380-965c-e3a9e3e3b28f" />
<img width="1146" height="435" alt="image" src="https://github.com/user-attachments/assets/63e06e45-fbbf-4ce5-a086-f499b018478f" />
-----

## 📊 Analytics & Dashboards

<img width="870" height="484" alt="image" src="https://github.com/user-attachments/assets/d5a28d97-3403-409b-a169-e309428919a5" />
[Check out the Live Dashboard](https://app.powerbi.com/groups/bcb09513-cf78-4bc5-8c43-97160bf00cc2/reports/ff912cdf-ea4f-48d7-9a35-3b87c75a07ff/90fe6c2152da0c2d451c?experience=power-bi)

The Gold layer directly feeds a Power BI data model, delivering actionable insights on:

  * **Revenue & Growth:** Total Sales, Units Sold, and Monthly Revenue Trends.
  * **Customer Behavior:** Repeat Customer Rates and Distribution by Region.
  * **Product Performance:** Sales split by Brand, Category, and Channel (Mobile vs. Website).

-----
## 📈 Business Outcomes

* **Eliminated manual data consolidation**, streamlining operations.
* **Reduced reporting turnaround** from hours to minutes.
* **Established a single source of truth** for enterprise analytics.
* **Enabled real-time, self-service reporting** for key stakeholders.
* **Built a scalable and extensible data foundation** to support future data growth.

---

## 🧠 Skills & Concepts Learned

* Azure Data Lake Storage Gen2 (ADLS)
* Azure Databricks & Databricks Jobs
* Delta Lake & Medallion Architecture
* Unity Catalog & ETL / ELT Pipeline Design
* Data Quality & Validation Techniques
* Fact & Dimension Modeling (Star Schema)
* Incremental & Scheduled Data Processing
* Power BI Data Modeling & Visualization
* End-to-End Cloud Data Engineering

---

## 🧰 Tech Stack

* **Cloud:** Microsoft Azure
* **Storage:** Azure Data Lake Storage Gen2
* **Processing:** Azure Databricks (PySpark, SQL, Unity Catalog)
* **Data Format:** Delta Lake
* **Orchestration:** Databricks Jobs
* **Visualization:** Power BI


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

<img width="666" height="601" alt="image" src="https://github.com/user-attachments/assets/7394890d-4153-4c9e-9a4c-3642ce8609cf" />
<img width="1348" height="627" alt="image" src="https://github.com/user-attachments/assets/3fc158fe-8fa3-416c-b113-5e03e92b5086" />

----
## Started Data Timeline Jan 2024 to Aug 2025 (Historical Data) -- Dec 2025 (Incremental Data)
### Batch Processing: Collected data n process it all at once - every night data dropped at 11'o clock ETL job will load data in data warehouse triggered on schedule at every 2/4'o clock - Generate monthly financial data, daily summary data, Backfilling missing data.
### Stream Processing: As soon as data arrives - checkpointing for recovery (it saves the information which files are already processed)- almost real time monitoring PowerBI dashboard updates with seconds, Kafka for upstream - live analytics - constantly- daily on going basis - Stock market price analytics -  **design data pipeline such that it process it  automatically ** 

<img width="1188" height="318" alt="image" src="https://github.com/user-attachments/assets/f1ab15f5-3418-47d8-afe5-b3d14eb4372f" />
<img width="649" height="294" alt="image" src="https://github.com/user-attachments/assets/c7f17202-0f1d-44c8-b1b3-9c33457be9ad" />
<img width="650" height="301" alt="image" src="https://github.com/user-attachments/assets/352503e8-9abc-4ee3-83be-cfee4a93baf6" />

## 2_Medallion_Processing_dim - Historical data Processing

catalog_name = 'ecommerce' --- as variable later paramerterized with dbutils.widget
the third parameter means - False in schema - Can not have Null field in brand code as Primary key
<img width="1317" height="577" alt="image" src="https://github.com/user-attachments/assets/40ff0191-8edc-4a20-9a47-d562d44acc14" />
<img width="1206" height="558" alt="image" src="https://github.com/user-attachments/assets/c9db9648-558f-4696-b07c-6be835a03a35" />

Read csv files into a dataFrame first then write to a delta table - df.write.format("delta")
Through that raw connection - ingested data in bronze layer - and only dimension tables
- added metadata colums : source_file n ingested at
- ingest csv file write the data into delta table format so that it gets all the capabilities of like acid, time-travel - its essential component of Lakehouse architecture
- write n save it as delta in bronze layer create table as brz_bronze. for the first time write mode is overwrite and other mode is append mode for adding at the back - it's raw data
<img width="1298" height="542" alt="image" src="https://github.com/user-attachments/assets/0103bf0d-ec0f-46a9-ae0f-2bcd284a9a05" />
<img width="1288" height="582" alt="image" src="https://github.com/user-attachments/assets/3f57b470-cd95-431f-ae65-355cae34261e" />
<img width="1203" height="612" alt="image" src="https://github.com/user-attachments/assets/db3bcd12-55d1-4730-8d41-be9f8dbc5e3d" />

<img width="1300" height="634" alt="image" src="https://github.com/user-attachments/assets/a5a9f586-34cb-4615-8d77-8c0c5ca14d44" />

<img width="1308" height="562" alt="image" src="https://github.com/user-attachments/assets/9d95f11e-edd7-4e7f-a2b8-173d07a5fe87" />
<img width="1267" height="525" alt="image" src="https://github.com/user-attachments/assets/434f49e6-94f4-4247-b673-b1e6e5f37a3d" />

## 3_Medallion_Processing_fact -- Incremental Data Processing

<img width="1288" height="566" alt="image" src="https://github.com/user-attachments/assets/2c991297-d5f5-4f14-b3df-c3a5d37e3da6" />
<img width="1277" height="631" alt="image" src="https://github.com/user-attachments/assets/874afc03-3af9-40a0-90fa-0b17cd9f1419" />

<img width="655" height="569" alt="image" src="https://github.com/user-attachments/assets/e525a829-1fee-4b3b-93b1-0436b1540325" />
<img width="1255" height="509" alt="image" src="https://github.com/user-attachments/assets/6439faab-48bc-4cad-8957-c8793bb43842" />

### readStream - Structured Streaming API

- create delta table in ecommerce catalog.bronze ---- bronze.brz_order_items
- create checkpoint in adls - ecomm-raw-data > checkpoint
- check ingested file count
  
<img width="1354" height="488" alt="image" src="https://github.com/user-attachments/assets/06aa6d32-3b81-48c9-9c68-70f3db5357f2" />
<img width="1253" height="418" alt="image" src="https://github.com/user-attachments/assets/f685938c-8964-4eaf-91b8-7d1fa26a775c" />
<img width="1229" height="481" alt="image" src="https://github.com/user-attachments/assets/e59cf8dd-6c45-4f5a-9634-645a4129483f" />
<img width="1171" height="467" alt="image" src="https://github.com/user-attachments/assets/26b9defb-a049-4d7a-9dec-d112b2cc4fea" />
<img width="1164" height="434" alt="image" src="https://github.com/user-attachments/assets/c4810340-6e46-4bf2-953e-6b129cd2bca2" />
<img width="662" height="549" alt="image" src="https://github.com/user-attachments/assets/b42058f2-055a-4c9a-bde6-896a768a5cc7" />

- fact silver
<img width="1261" height="508" alt="image" src="https://github.com/user-attachments/assets/823572fd-299e-4336-a886-205ce673eecd" />
<img width="1294" height="608" alt="image" src="https://github.com/user-attachments/assets/cdfa46bc-37b0-4e2c-903f-fa55c4cd8d3c" />
<img width="637" height="591" alt="image" src="https://github.com/user-attachments/assets/c46e27bf-2136-489f-9d0b-5778be5d4261" />
<img width="658" height="493" alt="image" src="https://github.com/user-attachments/assets/659bd1fb-db93-4d1b-a7bb-37c7045e5bc2" />
<img width="1248" height="492" alt="image" src="https://github.com/user-attachments/assets/65ec9723-bd10-422c-832f-7e1ca20e04d3" />
<img width="652" height="441" alt="image" src="https://github.com/user-attachments/assets/7b4bfd7d-ef56-4490-bc38-22a37b4cfe88" />
<img width="646" height="496" alt="image" src="https://github.com/user-attachments/assets/f3bd1330-5d47-416c-90c5-b52c10f903a1" />

- fact gold 
<img width="973" height="549" alt="image" src="https://github.com/user-attachments/assets/2207378b-5e85-4b73-8326-8ca48e280b25" />
<img width="1039" height="518" alt="image" src="https://github.com/user-attachments/assets/4b1f2a80-0784-498a-bcdf-24f7c9bd94df" />

- Daily summary table
<img width="1354" height="624" alt="image" src="https://github.com/user-attachments/assets/57dd120e-5f68-470b-8cf1-2ab2d2bbfd99" />
<img width="1357" height="637" alt="image" src="https://github.com/user-attachments/assets/2a961b2c-fd63-4998-96f6-1a4e5c203c76" />
<img width="1353" height="626" alt="image" src="https://github.com/user-attachments/assets/e9784dd3-7b3c-4d3d-803f-5e01f0627b81" />




### Autoloader is a streaming ingestion feature designed to efficiently n automatically process new data files as they arrive in cloud storage - ADLS, S3 - in our case - in adls ecomm order_item - landing foldr daily someone is dropping new files n then we need to only process new files efficiently figure out - autoloader is feature which provide that functionality -- using pyspark module argument is CloudFiles : go to adls location n use autoloader to observe the file which are new don't process the old, it keeps track of old files what is processed. 

### Structured Streaming : Is a stream processing engine that uses unified API to process both batch n stream processing

### Widgets - dbutils.widgets - is use in many ways to specify the storage acount name or environment - dev/prod/beta - so the benefit is whenever running the same the notebook for different environment can update widgets and change the env and ok run all the cells n messing up with code for reconfigure parameter

### _resued_data - when you get new field it add it under here

### ChangeDataFeed = True in silver layer - _change_type - insert/update-pre or post/delete 
- CDF - track the changes in row level - more granular - useful for compliance
- df = 500000 Batch No 1 -100000, Batch no 2 - 100,000
- Upsert -- Already have table create an object delta table - Merge with existing table microBatch - trace

### Date object is bigger 21-06-2025 then Date_id - 21062025 is integer object - which makes things little faster

### Dimensional Pipeline - 
<img width="1340" height="610" alt="image" src="https://github.com/user-attachments/assets/3fb47fd3-bdf2-4902-82b4-0247bc326d91" />
<img width="1297" height="599" alt="image" src="https://github.com/user-attachments/assets/9fc4ae24-f112-4666-a026-a365a5c77ad5" />
<img width="1356" height="482" alt="image" src="https://github.com/user-attachments/assets/1834f57e-7616-4fbc-a649-e5b4b8549b27" />


### Fact Pipeline - 
<img width="1259" height="571" alt="image" src="https://github.com/user-attachments/assets/6f5ac588-f9cd-453f-820b-2227b2bb27e2" />
<img width="1117" height="571" alt="image" src="https://github.com/user-attachments/assets/1ba23ac2-7824-49c0-be49-901e5e5f2a8d" />
<img width="1117" height="551" alt="image" src="https://github.com/user-attachments/assets/9fc0b61d-c294-4801-af9c-6726c1177379" />


### Daily Refresh Job - task job - 
<img width="1334" height="333" alt="image" src="https://github.com/user-attachments/assets/52a1d15a-7cad-47b7-88bf-e040970959bf" />
<img width="1358" height="520" alt="image" src="https://github.com/user-attachments/assets/8e75bab3-f32a-4bd2-851f-62c897093b48" />
<img width="554" height="434" alt="image" src="https://github.com/user-attachments/assets/cd3d2809-064d-4b22-83b4-274190e1316e" />
<img width="1170" height="443" alt="image" src="https://github.com/user-attachments/assets/0c74d853-ece4-490b-8221-d57a7ef27a86" />
<img width="1164" height="545" alt="image" src="https://github.com/user-attachments/assets/edeedec5-c1b1-41b2-a64d-d45f7e29169b" />
<img width="857" height="447" alt="image" src="https://github.com/user-attachments/assets/adc1d752-3118-4bed-a472-657e632dbbee" />
<img width="849" height="405" alt="image" src="https://github.com/user-attachments/assets/c8201d8e-9779-41fe-853f-5d0f768d4be7" />
<img width="835" height="359" alt="image" src="https://github.com/user-attachments/assets/14cac95d-2937-4bdf-8968-127de645523f" />
<img width="1161" height="481" alt="image" src="https://github.com/user-attachments/assets/f7ba13e3-de68-4025-80c9-1a37355fb928" />
<img width="852" height="371" alt="image" src="https://github.com/user-attachments/assets/c729e60d-241c-44d4-ba67-2f5bffa1060f" />
<img width="1012" height="568" alt="image" src="https://github.com/user-attachments/assets/1296c67f-2d5f-4380-965c-e3a9e3e3b28f" />
<img width="1146" height="435" alt="image" src="https://github.com/user-attachments/assets/63e06e45-fbbf-4ce5-a086-f499b018478f" />


<img width="1301" height="593" alt="image" src="https://github.com/user-attachments/assets/fd995403-a68a-4797-af5c-bfd6b318a9b1" />




### Monthly Refresh Job - 

### Power BI

<img width="909" height="688" alt="image" src="https://github.com/user-attachments/assets/19e020c8-8709-4acb-b08c-294420ebe04c" />

<img width="722" height="378" alt="image" src="https://github.com/user-attachments/assets/bf777614-5b79-4026-a518-e8403fc04098" />
<img width="1346" height="545" alt="image" src="https://github.com/user-attachments/assets/8448b7f9-4eac-470d-8cd4-855e5e2c001b" />
<img width="790" height="360" alt="image" src="https://github.com/user-attachments/assets/3a0f9817-a144-4977-b648-39d396ab9dd3" />
<img width="1207" height="521" alt="image" src="https://github.com/user-attachments/assets/6df8dc00-08a7-477f-a3e9-a5c082239550" />
<img width="1005" height="302" alt="image" src="https://github.com/user-attachments/assets/637797ad-6156-46d1-b59c-f5d4ecc83fd4" />

<img width="798" height="474" alt="image" src="https://github.com/user-attachments/assets/62c0ab0a-4b54-463f-9f57-17ecf15a66a3" />
<img width="840" height="538" alt="image" src="https://github.com/user-attachments/assets/c7c5dc4e-8fee-4832-8966-58b0aae55e6a" />



---

