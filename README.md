# 🚀 End-to-End Data Engineering Solution with Azure

This project demonstrates how i built a **complete data engineering pipeline** on Microsoft Azure. It processes, transforms, and delivers data for **Business Intelligence (BI)** using **Azure Data Factory, Databricks, Synapse Analytics, and Power BI**.  

The data source is the **AdventureWorks dataset**, ingested directly from GitHub and transformed into a star-schema model for reporting. 
so this is the whole archietecture of my project-

![Architecture](https://github.com/user-attachments/assets/7c51260a-236e-43ae-a965-91508684014c)


---

## 🔹 Architecture Overview

### **Step 1: Setting Up Azure Environment**
Provisioned resources:
- **Azure Data Factory (ADF):** Data orchestration & automation.  
- **Azure Storage Account:** Acts as Data Lake (Bronze → Silver → Gold).  
- **Azure Databricks:** Performs large-scale transformations.  
- **Azure Synapse Analytics:** Data warehouse for BI.  

> Configured with IAM roles for secure integration.
> these were the resources used

![Setup](https://github.com/Harshita075/data-engineering-azure-project-adventure-works/blob/main/dataset/resource-groups.png)

---

### **Step 2: Data Ingestion with ADF** 🚀
- Built a **Dynamic Copy Activity** pipeline.  
- Pulled data from GitHub via HTTP connector → stored in **Bronze container**.  
- Used parameters for adaptability (file name, path, etc.).  

created the dynamic pipeline successfully-
![Adf](https://github.com/Harshita075/data-engineering-azure-project-adventure-works/blob/main/dataset/dynamic_pipeline.png)


---

### **Step 3: Transformation with Azure Databricks** 🔄
- Created **Databricks cluster** for scalable compute.  
- Connected to Data Lake (Bronze → Silver).  
- Applied transformations:  
  - Normalized **date formats**.  
  - Removed **invalid/incomplete records**.  
  - Grouped & aggregated data for analysis.  
- Stored results in **Parquet format** (efficient for queries).
- ![databricks](https://github.com/Harshita075/data-engineering-azure-project-adventure-works/blob/main/dataset/IMG_4561.jpg)


  did the transformations using PYSPARK-
  ![transform](https://github.com/Harshita075/data-engineering-azure-project-adventure-works/blob/main/dataset/Screenshot%20(81).png)
---

### **Step 4: Data Warehousing with Synapse Analytics** 📊
- Configured Synapse to connect with **Silver data**.  
- Used **Serverless SQL Pools** for querying without provisioning.  
- Designed **Database + Schema** → created external tables.  
- Modeled a **Star Schema** (Fact & Dimension tables).  



---

### **Step 5: Business Intelligence with Power BI** 📈
- Connected **Power BI** to Synapse.  
- Built dashboards to visualize KPIs (Sales, Revenue, Products, Regions).  



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

 ---
✨ This project was designed and implemented by **Harshita Ahuja** as part of my journey in mastering Data Engineering with Azure.  

