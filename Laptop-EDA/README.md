# 📊 Laptop Dataset EDA using PySpark

## 📌 Project Overview
This project focuses on **Exploratory Data Analysis (EDA)** of a **Laptop dataset** using **PySpark**.  
The goal is to understand data distribution, detect missing values & outliers, and extract meaningful insights that can support further analytics or machine learning models.

---

## 🛠️ Tech Stack
- **Python**
- **PySpark (Spark SQL & DataFrame API)**
- **Jupyter Notebook**
- **Apache Spark**

---

## 📂 Dataset Description
The dataset contains laptop-related attributes such as:
- Brand
- Processor
- RAM
- Storage
- Operating System
- Price
- Screen Size (if available)

📌 *Dataset used only for analytical purposes.*

---

## 🔍 EDA Steps Performed
- Schema inspection & data types validation  
- Null & missing value analysis  
- Duplicate record checks  
- Numerical feature distribution analysis  
- Categorical feature frequency analysis  
- Price-based segmentation  
- Brand-wise & configuration-wise comparison  

---

## 🧠 Key Insights
- Price variation is highly influenced by **RAM, Processor, and Storage**
- Certain brands dominate the mid-range pricing segment
- High-end configurations show significant price dispersion
- Missing values were minimal and handled appropriately

---

## 🧪 Sample PySpark Code
```python
from pyspark.sql import SparkSession
from pyspark.sql.functions import col

spark = SparkSession.builder \
    .appName("Laptop EDA") \
    .getOrCreate()

df = spark.read.csv("laptop_dataset.csv", header=True, inferSchema=True)

df.printSchema()
df.describe().show()

df.groupBy("brand").count().orderBy("count", ascending=False).show()

