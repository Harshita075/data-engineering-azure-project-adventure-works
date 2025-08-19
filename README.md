# 🚀 End-to-End Data Engineering Solution with Azure

This project demonstrates how to build a **complete data engineering pipeline** on Microsoft Azure. It processes, transforms, and delivers data for **Business Intelligence (BI)** using **Azure Data Factory, Databricks, Synapse Analytics, and Power BI**.  

The data source is the **AdventureWorks dataset**, ingested directly from GitHub and transformed into a star-schema model for reporting.  

![Architecture]()

---

## 🔹 Architecture Overview

### **Step 1: Setting Up Azure Environment**
Provisioned resources:
- **Azure Data Factory (ADF):** Data orchestration & automation.  
- **Azure Storage Account:** Acts as Data Lake (Bronze → Silver → Gold).  
- **Azure Databricks:** Performs large-scale transformations.  
- **Azure Synapse Analytics:** Data warehouse for BI.  

> Configured with IAM roles for secure integration.  

![Setup](https://github.com/Harshita075/data-engineering-azure-project-adventure-works/blob/main/archive/resource-groups.png)

---

### **Step 2: Data Ingestion with ADF** 🚀
- Built a **Dynamic Copy Activity** pipeline.  
- Pulled data from GitHub via HTTP connector → stored in **Bronze container**.  
- Used parameters for adaptability (file name, path, etc.).  

![ADF]()

---

### **Step 3: Transformation with Azure Databricks** 🔄
- Created **Databricks cluster** for scalable compute.  
- Connected to Data Lake (Bronze → Silver).  
- Applied transformations:  
  - Normalized **date formats**.  
  - Removed **invalid/incomplete records**.  
  - Grouped & aggregated data for analysis.  
- Stored results in **Parquet format** (efficient for queries).  

![Databricks]()

---

### **Step 4: Data Warehousing with Synapse Analytics** 📊
- Configured Synapse to connect with **Silver data**.  
- Used **Serverless SQL Pools** for querying without provisioning.  
- Designed **Database + Schema** → created external tables.  
- Modeled a **Star Schema** (Fact & Dimension tables).  

![Synapse](https://github.com/user-attachments/assets/ce425f1d-dcd9-4b99-85d1-acbbc9e50d82)

---

### **Step 5: Business Intelligence with Power BI** 📈
- Connected **Power BI** to Synapse.  
- Built dashboards to visualize KPIs (Sales, Revenue, Products, Regions).  

![PowerBI](https://github.com/user-attachments/assets/a195d455-5889-4042-b144-bfe89f4260ee)

---

## 🌟 Key Features & Takeaways
✔ **End-to-End Pipeline** → from raw GitHub data to BI dashboards.  
✔ **Automation** → ADF pipelines orchestrating all tasks.  
✔ **Scalability** → Databricks handles large-scale transformations.  
✔ **Efficiency** → Parquet format + Synapse SQL Pools = fast queries.  
✔ **Insights** → Interactive dashboards for decision-making.  

---

## 💡 Challenges Faced
- **Schema Drift:** Handled changing file structures using dynamic ADF pipelines.  
- **Data Cleaning Complexity:** Ensured data consistency before loading into Synapse.  
- **Integration Issues:** Solved access/authentication between Databricks & Synapse.  

---

## 📌 Tools & Technologies
- **Azure Data Factory**  
- **Azure Data Lake (Storage Account)**  
- **Azure Databricks (PySpark)**  
- **Azure Synapse Analytics**  
- **Power BI**  
- **GitHub (Data Source)**  

---

## 🙌 Acknowledgment
Inspired by [Ansh Lamba](https://github.com/anshlambagit).  
Check his [YouTube walkthrough](https://www.youtube.com/watch?v=0GTZ-12hYtU&t=15907s&ab_channel=AnshLamba) for more details.  

---

✅ This project is a **complete Azure Data Engineering solution**, perfect for showcasing in interviews & portfolios.
