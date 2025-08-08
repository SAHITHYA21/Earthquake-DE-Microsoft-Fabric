# 🌍 Earthquake Data Engineering Project with Microsoft Fabric

## 📌 Project Overview
This project demonstrates the development of an **end-to-end data engineering and analytics pipeline** for processing **global earthquake events**.  
Leveraging **Microsoft Fabric’s Data Factory, Data Engineering, and Power BI** capabilities, the solution automates the ingestion, cleaning, transformation, and visualization of real-time earthquake data from the **United States Geological Survey (USGS) API**.

The pipeline follows a **multi-layer architecture**:
- **Bronze Layer** → Raw data ingestion
- **Silver Layer** → Data cleaning and standardization
- **Gold Layer** → Business-ready datasets optimized for analytics

This architecture ensures **data accuracy, scalability, and performance optimization**, enabling analysts and stakeholders to extract valuable insights quickly.

---

## 🛠️ Technologies Used
- **Programming:** Python, PySpark  
- **Data Platform:** Microsoft Fabric (Data Factory, Data Engineering)  
- **Visualization:** Power BI  
- **Data Source:** USGS Earthquake Events API  

---

## 📂 Repository Contents

### 1️⃣ Bronze Layer – Raw Data Ingestion
- Connects to the **USGS API** to fetch worldwide earthquake events.  
- Stores the data in its raw form to maintain data integrity.  
- Performs minimal preprocessing (e.g., schema definition, timestamp parsing).  

**Key Goal:** Preserve original data for historical tracking and reproducibility.

---

### 2️⃣ Silver Layer – Data Cleaning & Transformation
- Handles missing values, type casting, and field normalization.  
- Converts raw JSON into structured tables for easy querying.  
- Integrates geospatial attributes for mapping capabilities in Power BI.  

**Key Goal:** Provide a standardized, high-quality dataset for analytics.

---

### 3️⃣ Gold Layer – Analytics-Ready Datasets
- Aggregates and enriches data for analytical use cases.  
- Optimizes storage formats (e.g., Delta/Parquet) for fast querying.  
- Prepares datasets for specific reporting purposes such as **trend analysis, magnitude distribution, and regional impact studies**.  

**Key Goal:** Deliver business-ready datasets for decision-making and reporting.

---

## 📊 Data Attributes

| Attribute           | Type     | Description |
|---------------------|----------|-------------|
| `id`                | String   | Unique identifier for each earthquake record |
| `latitude`          | Double   | Latitude of the event location |
| `longitude`         | Double   | Longitude of the event location |
| `elevation`         | Double   | Elevation in meters where the event occurred |
| `title`             | String   | Title or name of the earthquake event |
| `place_description` | String   | Location description of the event |
| `sig`               | BigInt   | Significance score of the event |
| `mag`               | Double   | Magnitude of the earthquake |
| `magType`           | String   | Type of magnitude scale used |
| `time`              | Timestamp| Exact time of the event |
| `updated`           | Timestamp| Last update time of the event data |

---

## 📈 Project Workflow

```plaintext
USGS API → Data Factory (Ingestion) → Bronze Layer (Raw Data)
→ Silver Layer (Cleaned Data) → Gold Layer (Analytics-Ready Data)
→ Power BI Dashboards (Visualization & Insights)
