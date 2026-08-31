# Databricks
Spark Data Analytics and MLib 

1. Medallion Architecture 
- Bronze : Import file from Kaggle onto Databricks Notebook (Bronze Layer) using Token APIs
- Silver : Handle Duplication, Null Values, Remove Patient Name, RegEx(Regular Expression) and Add up Ingestion time, Filename, UUID (Patient ID)
- Gold : Data Analytics
2. Machine Learning 
- Feature Engineering (String Indexer, One Hot Encoding)
- Apply Models (Linear Regression, Decision Tree)
- Pipeline
- Evaluate (R2 & RMSE)
