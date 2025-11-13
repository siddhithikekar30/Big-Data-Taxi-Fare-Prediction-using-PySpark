# 🚖 NYC Taxi Big Data Fare Calculation Project

This repository contains a comprehensive **PySpark-based Big Data pipeline** for calculating taxi fares using the NYC Taxi dataset. The workflow demonstrates scalable data processing, feature engineering, exploratory analysis, and performance-optimized transformations suited for large datasets.

---

## 📌 Project Overview

This project showcases:

* Loading and processing millions of rows of NYC Taxi trip data
* Cleaning, filtering, and preparing structured datasets
* Engineering key features for fare prediction and analysis
* Computing descriptive statistics using PySpark
* Evaluating fare distribution and geospatial patterns

The notebook (*big-data-fare-calculation.ipynb*) walks through the entire workflow end-to-end.

---

## 🛠️ Tech Stack

* **PySpark** (RDDs + DataFrames)
* **Python 3.x**
* **Jupyter Notebook**
* **NYC Taxi Open Data**

---

## 📁 Files in This Repository

* `big-data-fare-calculation.ipynb` – Main notebook containing the full pipeline
* `README.md` – Project documentation (you are reading it)

---

## 🔍 Key Features Implemented

### ✔️ Data Loading & Schema Inference

Efficiently loads large CSV files using Spark DataFrames with an optimized schema.

### ✔️ Data Cleaning & Preprocessing

* Removing invalid trips (negative distance/time, nulls)
* Filtering outliers in fare amount and trip duration
* Parsing timestamps and computing trip features

### ✔️ Feature Engineering

* Trip distance bands
* Peak vs off-peak hours
* Borough-based pickup and drop-off logic
* Seasonal effects using month/day extraction

### ✔️ Fare Analysis

* Average fare vs distance
* Fare distribution plots
* Identifying anomalies (very high/low fares)
* Surge-like effects during peak time windows

---

## 📊 Sample Results (High-Level Summary)

* **Mean Fare:** Varies by distance, time of day, and pickup zone
* **Long trips** (>12 miles) show non-linear increases in fare
* **Peak hours** show higher average fares per mile
* **Airport trips** (JFK/LGA) show distinct fare patterns

---

## ▶️ How to Run

1. Install dependencies:

   ```bash
   pip install pyspark
   ```
2. Open the notebook:

   ```bash
   jupyter notebook big-data-fare-calculation.ipynb
   ```
3. Run all cells in order for complete workflow.

---

## 🧠 Learnings & Takeaways

* Large NYC Taxi datasets require **distributed computing** for efficient processing
* Data cleaning is the most critical step before any meaningful analysis
* PySpark makes it possible to run complex transformations at scale
* Feature engineering drastically improves pattern understanding

---

## ⭐ Future Improvements

* Build a full **fare prediction machine learning model** using PySpark MLlib
* Add geospatial mapping for visualization (Folium/KeplerGL)
* Implement a Spark SQL layer for interactive querying
* Deploy the pipeline on AWS EMR or Databricks

---

## 🤝 Contributing

Feel free to open issues or submit pull requests for improvements.

---

## 📜 License

This project is licensed under the MIT License.

---

If you like this project, don't forget to ⭐ star the repository!
