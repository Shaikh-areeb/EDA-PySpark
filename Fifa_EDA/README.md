# ⚽ FIFA Dataset EDA using PySpark

## 📌 Project Overview

Performed **Exploratory Data Analysis (EDA)** on the FIFA dataset using **PySpark** to understand player attributes, salary distribution, and categorical patterns.

## 🛠 Tools

* Python
* PySpark
* Jupyter Notebook

## 🔍 Analysis Performed

* Loaded dataset into a PySpark DataFrame and inspected schema & columns
* Analyzed **missing values** across numerical and categorical features
* Handled null values:

  * Numerical columns → filled using **mean**
  * Categorical columns → filled using **mode**
* Created a new feature **Salary_Flag** using conditional logic (`when`, `otherwise`)
* Performed **group-based aggregations** using:

  * `groupBy()`
  * `count()`
  * `avg()`
  * `sum()`
* Explored **categorical distributions** such as player positions
* Analyzed **salary distribution** and player wage patterns
* Calculated **quantiles and percentiles** for statistical insights

## 📊 Key Learnings

* PySpark DataFrame transformations
* Null value handling strategies
* Aggregations and grouping
* Feature engineering
* Statistical exploration using PySpark

