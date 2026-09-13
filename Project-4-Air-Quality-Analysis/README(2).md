# 🌍 Air Quality Analysis

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python" alt="Python">
  <img src="https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=for-the-badge&logo=pandas" alt="Pandas">
  <img src="https://img.shields.io/badge/Matplotlib-Visualization-11557c?style=for-the-badge" alt="Matplotlib">
  <img src="https://img.shields.io/badge/Seaborn-Visualization-4c72b0?style=for-the-badge" alt="Seaborn">
  <img src="https://img.shields.io/badge/Jupyter-Notebook-orange?style=for-the-badge&logo=jupyter" alt="Jupyter">
</p>

<p align="center">
  <b>Exploratory Data Analysis of Air Quality, Pollution Patterns & Weather Relationships</b>
</p>

---

## 📌 Project Overview

**Air Quality Analysis** is a data analysis project focused on exploring air pollution measurements and understanding how pollutant levels vary across **time** and in relation to **weather conditions**.

The project applies a complete data-analysis workflow:

> **Raw Data → Data Cleaning → Feature Engineering → EDA → Time Analysis → Correlation Analysis → Visualization → Insights → Export**

The analysis is designed to identify meaningful patterns in pollutant concentrations, compare pollution across different time periods, study relationships between pollutants and weather variables, and communicate the results through clear visualizations.

---

## 🎯 Objectives

- Clean and prepare air-quality data for analysis.
- Explore pollutant distributions and descriptive statistics.
- Analyze pollution patterns by **day, hour, month, weekday and weekend**.
- Study relationships between pollutants and weather conditions.
- Calculate and visualize correlation patterns.
- Identify important pollution peaks and variations.
- Create professional visualizations for data interpretation.
- Export cleaned and analytical datasets for further use.

---

## 🗂️ Dataset

The project uses an **Air Quality dataset** containing hourly measurements of air pollutants and environmental variables.

### Main pollutant measurements

| Feature | Description |
|---|---|
| `CO(GT)` | Carbon Monoxide |
| `NMHC(GT)` | Non-Methane Hydrocarbons |
| `C6H6(GT)` | Benzene |
| `NOx(GT)` | Nitrogen Oxides |
| `NO2(GT)` | Nitrogen Dioxide |

### Weather / environmental variables

| Feature | Description |
|---|---|
| `T` | Temperature |
| `RH` | Relative Humidity |
| `AH` | Absolute Humidity |

### Time variables

The dataset also contains:

- `Date`
- `Time`
- `DateTime`
- `Year`
- `Month`
- `Day`
- `Hour`
- `Month_Name`
- `Day_Name`
- `Day_Type`

---

## 🛠️ Tools & Technologies

- **Python**
- **Pandas** — data manipulation and analysis
- **NumPy** — numerical operations
- **Matplotlib** — data visualization
- **Seaborn** — statistical visualization
- **Jupyter Notebook / Google Colab** — development environment

---

## 🔄 Project Workflow

### 1️⃣ Data Loading
The dataset is loaded into a Pandas DataFrame and its structure, columns, data types and basic statistics are inspected.

### 2️⃣ Data Cleaning
The data is prepared for reliable analysis by handling invalid/missing measurements and preparing the required columns.

### 3️⃣ Date & Time Processing
Separate date and time information is combined into a proper `DateTime` column.

Additional time-based features are extracted for detailed analysis.

### 4️⃣ Exploratory Data Analysis
The project examines:

- Descriptive statistics
- Distributions
- Outliers
- Average pollutant levels
- Pollutant variability

### 5️⃣ Time-Based Analysis
Pollution is analyzed across:

- Daily trends
- Hourly patterns
- Monthly patterns
- Weekdays vs weekends

### 6️⃣ Relationship Analysis
Correlation analysis is performed between:

- Pollutants
- Pollutants and temperature
- Pollutants and relative humidity
- Pollutants and absolute humidity

### 7️⃣ Visualization
The notebook contains professional visualizations including:

- Bar charts
- Histograms
- Boxplots
- Line charts
- Scatter/regression plots
- Correlation heatmaps
- Comparison charts

### 8️⃣ Final Insights
The analysis automatically identifies important patterns such as:

- Highest average pollutant
- Lowest average pollutant
- Most variable pollutant
- Peak pollution hour
- Peak pollution month
- Strong pollutant correlations
- Important weather relationships

---

## 📊 Key Analysis Areas

### 🔬 Pollutant Analysis
The project compares pollutant concentrations using descriptive statistics and visualizations.

### ⏰ Hourly Analysis
Hourly averages help identify periods of relatively higher or lower pollution.

### 📅 Daily & Monthly Analysis
Time-series and monthly aggregation help reveal longer-term pollution patterns.

### 🌡️ Weather Relationship
Pollutant levels are compared with temperature and humidity variables to identify statistical relationships.

### 🔗 Correlation Analysis
Correlation matrices are used to measure the strength and direction of relationships between numerical variables.

> **Note:** Correlation indicates statistical association and should not be interpreted as proof of causation.

---

## 📁 Repository Structure

```text
Air-Quality-Analysis/
│
├── Air_Quality_Analysis.ipynb
├── air_quality_cleaned.csv
├── pollutant_summary.csv
├── pollutant_weather_correlations.csv
└── README.md
```

### File Description

| File | Purpose |
|---|---|
| `Air_Quality_Analysis.ipynb` | Complete analysis notebook |
| `air_quality_cleaned.csv` | Cleaned dataset used for analysis |
| `pollutant_summary.csv` | Statistical summary of pollutant variables |
| `pollutant_weather_correlations.csv` | Correlation results between pollutants and weather variables |
| `README.md` | Project documentation |

---

## 📈 Expected Outputs

The notebook produces:

- Pollutant summary statistics
- Distribution plots
- Outlier analysis
- Daily pollution trends
- Hourly pollution patterns
- Monthly pollution patterns
- Weather relationship plots
- Correlation heatmaps
- Weekday/weekend comparisons
- Final analytical summary

All numerical findings are generated from the dataset through Python rather than manually entered.

---

## 💡 Project Value

This project demonstrates practical skills in:

- Data Cleaning
- Exploratory Data Analysis (EDA)
- Feature Engineering
- Time-Series Aggregation
- Statistical Correlation
- Data Visualization
- Analytical Interpretation
- Python/Pandas Workflow
- Data Export & Reporting

---

## ⚠️ Limitations

- Correlation analysis does not establish causation.
- Missing/invalid sensor measurements can affect statistical results.
- The dataset represents measurements from its specific monitoring environment and time period.
- Pollution levels may be influenced by factors not included in the dataset.
- Different pollutants have different units/scales, so direct visual comparison should be interpreted carefully.

---

## 🚀 Future Scope

Possible extensions include:

- Air-quality forecasting using machine learning.
- Pollution-level prediction models.
- Interactive dashboards using **Power BI**, **Tableau**, or **Plotly**.
- Anomaly detection for unusual pollution events.
- More advanced time-series forecasting.
- Additional external weather and traffic data integration.

---

## 👨‍💻 Project Information

| Detail | Information |
|---|---|
| **Project** | Air Quality Analysis |
| **Author** | Chand Khimani |
| **Instructor** | Girish Gondaliya |
| **Course** | BCA Data Analysis |

---

## 🏁 Conclusion

The **Air Quality Analysis** project provides a structured exploratory analysis of pollutant measurements and environmental conditions.

Through data cleaning, feature engineering, statistical analysis, time-based aggregation, correlation analysis and visualization, the project creates a clear analytical workflow for understanding air-quality data.

The notebook is designed so that the final findings are derived directly from the dataset, making the analysis reproducible and suitable for further exploration or machine-learning applications.

---

## ⭐ Skills Demonstrated

`Python` · `Pandas` · `NumPy` · `Matplotlib` · `Seaborn` · `EDA` · `Data Cleaning` · `Feature Engineering` · `Correlation Analysis` · `Data Visualization` · `Time-Based Analysis`

---

<p align="center">
  <b>🌱 Data-driven analysis for a better understanding of air quality.</b>
</p>
