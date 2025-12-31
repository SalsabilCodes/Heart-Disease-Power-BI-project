# Heart Disease Clinical Insights & Risk Analysis

This project analyzes clinical cardiovascular data to identify key risk factors and patterns associated with heart disease. The analysis provides actionable health insights through interactive visualizations, helping to understand how demographics (age, sex) and clinical metrics (cholesterol, blood pressure, ECG) correlate with the presence of heart disease.

**Project Status: Completed**

## Project Overview
The project focuses on heart disease prevalence and the impact of various medical indicators. It includes detailed breakdowns by gender, age groups, chest pain types, and exercise-induced conditions. It features custom health-related KPIs and visualization-friendly data modeling in Power BI to support clinical decision-making and risk assessment.

## Data Source
The dataset was sourced from **Kaggle**: [Heart Disease Prediction Dataset](https://www.kaggle.com/datasets/neurocipher/heartdisease). It contains 270 clinical records with 13 attributes and a target variable indicating the presence or absence of heart disease.

## Methods Used
* **Data Transformation & Cleaning** using Power Query.
* **Data Modeling** and relationship management in Power BI.
* **Descriptive Analysis** to calculate prevalence and averages.
* **Comparative Analysis** (Gender-based risk, Age-group distribution).
* **Categorization & Segmentation** (High/Normal blood sugar, Exercise-induced symptoms).

## Technologies
* **Power BI** (for Data Modeling and Visualization).
* **Power Query** (for ETL and Data Cleaning).
* **DAX (Data Analysis Expressions)** for creating dynamic medical measures and KPIs.

## Project Details

### Data Cleaning (Power Query)
* **Sex:** Converted from integer (0, 1) to Text: `1 = Male`, `0 = Female`.
* **FBS over 120:** Converted from integer (0, 1) to Text: `1 = High`, `0 = Normal`.
* **Exercise angina:** Converted from integer (0, 1) to Text: `1 = Yes`, `0 = No`.
* **Data Types:** Standardized clinical columns (Age, BP, Cholesterol) to numerical formats and categorical columns to text for better grouping.

### Power BI Data Modeling & DAX
* **Total Patients:** `Total Patients = COUNTROWS('Heart_Disease_Prediction')`
* **Patients with Disease:** `CALCULATE([Total Patients], 'Heart_Disease_Prediction'[Heart Disease] = "Presence")`
* **Prevalence Rate (%):** `Prevalence % = DIVIDE([Patients with Disease], [Total Patients], 0)`
* **Average Vitals:** Created measures for `Avg Age`, `Avg BP`, and `Avg Cholesterol`.
* **Risk Metrics:** Developed dynamic measures to calculate the impact of `Exercise Angina` and `High FBS` on heart health using text-based filtering.

### Visualizations (Implemented in Power BI)
* **Executive Summary Cards:** Displaying Total Patients, Heart Disease Prevalence %, and Average Age.
* **Prevalence Donut Chart:** Showing the split between "Presence" vs. "Absence" of heart disease.
* **Chest Pain Risk Analysis:** Bar chart correlating chest pain types with the highest disease prevalence.
* **Risk Slicers:** Dynamic filters for Gender, Fasting Blood Sugar (High/Normal), and Exercise-induced Angina (Yes/No).
* **Age Trend Analysis:** Visualizing how the probability of disease increases across different age groups.

## How to Use This Repository
1. Clone or download the repository.
2. Use the `Heart_Disease_Prediction.csv` file as the data source.
3. Load the dataset into Power BI.
4. Apply the **Power Query** steps mentioned in the "Data Cleaning" section.
5. Use the provided **DAX measures** to reproduce the analysis and KPIs.
6. Customize the reports and visualizations as needed.
