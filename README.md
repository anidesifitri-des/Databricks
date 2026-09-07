# Databricks Spark Data Analytics and MLib (Batch Processing)

**End to End Healthcare Data Pipeline & Machine Learning**

# Description
* This project is Implemented end to end Data Pipeline by Leveraging Medallion Architecture (Bronze, Silver, Gold) and continuing to apply Machine Learning 
* Dataset was used from Kaggle (Healthcare Dataset), with Batch Processing Method
* Schema : Age, Gender, Blood Type, Medical Condition, Date of Admission, Doctor, Hospital, Insurance Provider, Billing Amount, Room Number, Admission Type, Discharge Date, Medication, Test Result 

# Technology that used on this project
* Environment : Databricks
* Programming Language : Python (Apache Spark)
* Storage : DBFS (Databricks File Management Systems - Databricks Cloud)
  - Bronze Layer   : CSV to Parquet
  - Silver Layer   : Parquet
  - Gold Layer     : Parquet to Delta Lake
* Machine Learning : Spark Mlib

# Architecture Data (Medallion Architecture)  
Pipeline divided into four steps
- Bronze_Layer : Import raw data (CSV) from Kaggle onto Databricks Notebook (Bronze Layer) using Token APIs
- Silver_Layer : Handle Duplication, Null Values, Format Standarization (Remove Patient Name, RegEx(Regular Expression) and Add up Ingestion time, Filename, UUID (Patient ID))
- Gold_Layer   : Data Analytics

# Results & Visualizations

 * Percentages of Total Patient divided by Medical Condition (Pie Chart)
 <img width="975" height="600" alt="visualization" src="https://github.com/user-attachments/assets/c30416c4-f02f-41b3-a67d-c224ca79a3cb" />

 * Distribution of Medical Condition (Line Chart)
 <img width="859" height="547" alt="image" src="https://github.com/user-attachments/assets/a2eca235-1fe9-459a-9c4e-7667d1971245" />

* Tied among Total Patient and Average Age Grouped by Medical Condition 
<img width="248" height="143" alt="Screenshot 2026-09-07 134757" src="https://github.com/user-attachments/assets/fa9554e6-7d2f-486e-a765-aee122c334c6" />

* Tied among Total Patient and Average Billing Grouped by Medical Condition, Insurance Provider
<img width="366" height="337" alt="image" src="https://github.com/user-attachments/assets/a37b8db7-604c-4e15-8651-45839fda385a" />

* Tied among Blood Type and Total Patient Grouped by Medical Condition 
<img width="242" height="340" alt="image" src="https://github.com/user-attachments/assets/ec159682-396f-4ff2-85b5-bc1f6cf549b7" />

* Correlation Pearson 
<img width="844" height="719" alt="image" src="https://github.com/user-attachments/assets/839e1972-03fe-4909-b246-63e527f10e18" />

# Machine Learning 
* Feature Engineering
  - Categorical Attributes : String Indexer (Label Encoding), One Hot Encoding (Binary Vectorixation)
  - Numerical Attributes : StandardScaler (Standardization)
  - Vector Assembler :
  - 
* Apply Models (Linear Regression, Decision Tree)
* Pipeline
* Evaluate (R2 & RMSE)
