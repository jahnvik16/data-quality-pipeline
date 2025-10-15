# 🧹 Data Quality Pipeline

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1XB_OCAzXOESPzv25KxluARHpU2lnHjOL?usp=sharing)

A Python-based pipeline for **automated dataset inspection, cleaning, and insight generation**.  
It loads tabular data (e.g. CSV), identifies missing values, outliers, and correlations, and produces
summary statistics and visualizations.  
A monitoring component (using Streamlit / Evidently AI) tracks data-quality metrics over time.

---

## 📋 Table of Contents
1. [Overview](#overview)
2. [Features](#features)
3. [Technologies](#technologies)
4. [Setup & Installation](#setup--installation)
5. [Usage](#usage)
6. [Output Examples](#output-examples)
7. [Monitoring Dashboard](#monitoring-dashboard)
8. [Project Structure](#project-structure)
9. [Future Improvements](#future-improvements)
10. [License](#license)

---

## 🧠 Overview
The **Data Quality Pipeline** automates data-preparation tasks that precede model building.  
It:
- Loads structured datasets  
- Performs data profiling  
- Cleans missing, duplicate, or inconsistent records  
- Detects outliers using the IQR method  
- Computes descriptive statistics and correlations  
- Generates visual reports (histograms, boxplots, heatmaps)  
- Optionally connects to a **monitoring dashboard** to track data-quality drift over time

---

## ✨ Features
- 📊 Automatic dataset profiling (shape, types, missing values)  
- 🔧 Data cleaning: imputation & duplicate removal  
- 📈 Exploratory plots (Matplotlib / Seaborn)  
- 🧮 Correlation and outlier detection  
- 🧠 Insight generation summary  
- 📉 Integration hooks for Streamlit/Evidently monitoring  

---

## 🧰 Technologies
| Category | Tools/Libraries |
|-----------|----------------|
| Core Language | Python 3 |
| Data Handling | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Monitoring (Optional) | Streamlit, Evidently AI |
| Environment | Google Colab |

---

## ⚙️ Setup & Installation
1. Open the notebook in **Google Colab**  
   [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1XB_OCAzXOESPzv25KxluARHpU2lnHjOL?usp=sharing)

2. Run the following cell to install dependencies:
   ```bash
   !pip install -r requirements.txt
3. Upload your dataset or use the sample data.csv created by the notebook.

▶️ Usage

1. Load Data

   import pandas as pd

   df = pd.read_csv('your_dataset.csv')

3. Inspect

   df.info()

   df.describe()

5. Clean
  Handle missing values
  Remove duplicates
  Detect outliers (IQR)

6. Visualize
   Histograms, boxplots, scatter plots

7. Generate Insights
  Summaries of missing values, skewness, correlations

8. Save Cleaned Data

df.to_csv('data_cleaned.csv', index=False)

📊 Output Examples

Typical outputs include:

Summary statistics (.describe() tables)

Missing-value report

Outlier summary

Histograms & boxplots

Correlation heatmap

Cleaned dataset: data_cleaned.csv

🧩 Monitoring Dashboard

The pipeline integrates with monitoring tools such as Streamlit or Evidently AI to track:

Missing-value trends

Outlier counts

Statistical drift between data versions

Processing latency and row-volume metrics

Example workflow:

The pipeline logs metrics to metrics_log.csv.

A Streamlit dashboard reads this file and visualizes:

Line charts of drift metrics

Alerts for threshold breaches

This allows long-term visibility into dataset health for production ML workflows.
