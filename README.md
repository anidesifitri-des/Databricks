# Databricks Spark Data Analytics and MLib 

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
+-----------------+-------------+-----------+
|Medical_Condition|Total_Patient|Average_Age|
+-----------------+-------------+-----------+
|     Hypertension|         9245|       51.7|
|         Diabetes|         9304|       51.6|
|           Cancer|         9227|       51.6|
|          Obesity|         9231|       51.2|
|           Asthma|         9185|       51.6|
|        Arthritis|         9308|       51.6|
+-----------------+-------------+-----------+

* Tied among Total Patient and Average Billing Grouped by Medical Condition, Insurance Provider 
+------------------+-----------------+-------------+---------------+
|Insurance_Provider|Medical_Condition|Total_Patient|Average_Billing|
+------------------+-----------------+-------------+---------------+
|             Cigna|           Asthma|         1907|   25610.471279|
|          Medicare|         Diabetes|         1903|   25671.451850|
|             Cigna|        Arthritis|         1900|   25318.173511|
|             Cigna|         Diabetes|         1893|   25651.208722|
|        Blue Cross|          Obesity|         1891|   26100.785193|
| United Healthcare|     Hypertension|         1888|   25215.652240|
|             Aetna|     Hypertension|         1876|   25896.214680|
| United Healthcare|        Arthritis|         1873|   25627.489973|
| United Healthcare|           Cancer|         1870|   24857.847380|
| United Healthcare|           Asthma|         1870|   25819.633770|
|          Medicare|           Cancer|         1866|   25337.967058|
|             Cigna|           Cancer|         1864|   25582.045536|
|             Cigna|          Obesity|         1864|   26116.999238|
|        Blue Cross|         Diabetes|         1860|   25820.047274|
|          Medicare|          Obesity|         1854|   25838.726375|
|        Blue Cross|        Arthritis|         1852|   25792.788639|
|          Medicare|        Arthritis|         1851|   25272.076596|
|          Medicare|     Hypertension|         1847|   25811.975582|
|             Aetna|         Diabetes|         1842|   25565.188236|
|        Blue Cross|           Asthma|         1835|   25141.777074|
+------------------+-----------------+-------------+---------------+

* Tied among Blood Type and Total Patient Grouped by Medical Condition 
+-----------------+----------+-------------+
|Medical_Condition|Blood_Type|Total_Patient|
+-----------------+----------+-------------+
|     Hypertension|       AB+|         1215|
|         Diabetes|        A+|         1213|
|        Arthritis|        B+|         1201|
|     Hypertension|        A-|         1199|
|        Arthritis|        O+|         1198|
|           Cancer|       AB-|         1198|
|           Cancer|        B+|         1196|
|        Arthritis|       AB-|         1192|
|           Asthma|       AB+|         1189|
|         Diabetes|        B+|         1188|
|          Obesity|        B-|         1188|
|           Cancer|        A+|         1185|
|          Obesity|        A+|         1179|
|     Hypertension|        B-|         1173|
|           Asthma|        A-|         1173|
|           Asthma|        O+|         1173|
|         Diabetes|       AB+|         1173|
|        Arthritis|        B-|         1169|
|         Diabetes|        A-|         1167|
|     Hypertension|        O+|         1157|
+-----------------+----------+-------------+

* Correlation Pearson 
<img width="844" height="719" alt="image" src="https://github.com/user-attachments/assets/839e1972-03fe-4909-b246-63e527f10e18" />

# Machine Learning 
- Feature Engineering (String Indexer, One Hot Encoding)
- Apply Models (Linear Regression, Decision Tree)
- Pipeline
- Evaluate (R2 & RMSE)
