# 🌍 Global Happiness Report Analysis

### Uncovering the Key Drivers of Happiness Across Countries (2015--2019)

A Python-based data analysis project exploring global happiness levels
across countries from **2015 to 2019**. The project covers data
cleaning, transformation, exploratory data analysis, correlation
analysis, country comparison, and visualization.

------------------------------------------------------------------------

## 📌 Project Overview

The **Global Happiness Report Analysis** combines World Happiness Report
datasets from 2015--2019 into a standardized dataset.

The analysis explores the relationship between happiness and factors
such as:

-   💰 GDP per Capita
-   👨‍👩‍👧 Social Support
-   ❤️ Life Expectancy
-   🕊️ Freedom
-   🎁 Generosity
-   🏛️ Perception of Corruption

> **Important:** Correlation shows association between variables and
> does not prove causation.

------------------------------------------------------------------------

## 🎯 Objectives

1.  Understand the structure and quality of the datasets.
2.  Clean and standardize data from different years.
3.  Combine yearly datasets into one master dataset.
4.  Explore happiness across countries and years.
5.  Analyze relationships between happiness and different factors.
6.  Compare high- and low-happiness country-year records.
7.  Identify factors most strongly associated with happiness.
8.  Present findings through clear visualizations.

------------------------------------------------------------------------

## ❓ Analytical Questions

-   What is the overall happiness level across the dataset?
-   Which countries recorded the highest happiness scores?
-   Which countries recorded the lowest happiness scores?
-   How did average happiness change between 2015 and 2019?
-   Which factors have the strongest relationship with happiness?
-   How do socioeconomic and social factors compare across countries?
-   What major patterns can be observed?

------------------------------------------------------------------------

## 📊 Dataset

### Data Used

World Happiness Report datasets covering:

**2015, 2016, 2017, 2018, and 2019**

The original files use different column names and structures, so
relevant variables were standardized before combining them.

### Standardized Variables

  Variable                  Description
  ------------------------- -----------------------------------
  `year`                    Report year
  `country`                 Country name
  `happiness_score`         Overall happiness score
  `gdp_per_capita`          Economic performance indicator
  `social_support`          Social/family support indicator
  `life_expectancy`         Healthy life expectancy indicator
  `freedom`                 Freedom to make life choices
  `generosity`              Generosity indicator
  `corruption_perception`   Perception of corruption

------------------------------------------------------------------------

## 🧹 Data Cleaning & Preparation

The project includes:

-   Loading all five yearly CSV files.
-   Checking dataset dimensions and column structures.
-   Checking missing values and duplicates.
-   Standardizing column names.
-   Harmonizing relevant variables across report editions.
-   Combining yearly datasets into a master dataset.
-   Handling the single missing `corruption_perception` value using
    median imputation.
-   Sorting and preparing the clean dataset.
-   Exporting the cleaned dataset as a CSV file.

------------------------------------------------------------------------

## 🔬 Analysis Performed

### 1. Data Understanding

-   Dataset dimensions
-   Column inspection
-   Data types
-   Missing value analysis
-   Duplicate checking
-   Country-year validation

### 2. Exploratory Data Analysis

-   Descriptive statistics
-   Happiness score distribution
-   Average happiness by year
-   Highest and lowest happiness scores
-   Top 10 happiest country-year records
-   Bottom 10 happiest country-year records

### 3. Correlation Analysis

Pearson correlation was calculated between happiness and:

-   GDP per Capita
-   Social Support
-   Life Expectancy
-   Freedom
-   Generosity
-   Corruption Perception

Correlation heatmaps and comparison charts are included.

### 4. Year-wise Analysis

The project compares:

-   Average happiness by year
-   Median happiness by year
-   Minimum and maximum happiness
-   Year-wise factor averages
-   Yearly factor trends

### 5. Country Comparison

The project examines:

-   Average happiness by country
-   Highest and lowest recorded happiness
-   Number of years observed
-   Top 10 happiest records
-   Bottom 10 happiest records

------------------------------------------------------------------------

## 📈 Key Findings

Based on the completed analysis:

### 🏆 Highest Recorded Happiness

**7.77 --- Finland (2019)**

### 📉 Lowest Recorded Happiness

**2.69 --- Central African Republic (2017)**

### 📊 Overall Average Happiness

Approximately **5.38** across the combined dataset.

### 🔎 Strongest Associated Factor

**GDP per Capita** shows the strongest association with happiness in the
combined dataset.

**Pearson correlation ≈ 0.789**

Other factors such as social support, life expectancy, and freedom also
show meaningful relationships with happiness.

> These findings describe patterns and associations in the dataset. They
> should not be interpreted as proof that a factor directly causes
> happiness.

------------------------------------------------------------------------

## 📊 Visualizations

The notebook includes:

-   📈 Average Happiness Trend
-   📊 Happiness Score Distribution
-   🔥 Correlation Heatmap
-   📉 Factor Correlation Chart
-   💰 GDP vs Happiness
-   👨‍👩‍👧 Social Support vs Happiness
-   ❤️ Life Expectancy vs Happiness
-   🕊️ Freedom vs Happiness
-   🎁 Generosity vs Happiness
-   🏛️ Corruption Perception vs Happiness
-   🏆 Top 10 Happiest Country-Year Records
-   📉 Bottom 10 Happiest Country-Year Records
-   🌎 Year-wise Country Comparisons

------------------------------------------------------------------------

## 🛠️ Technologies Used

-   **Python**
-   **Pandas** --- data manipulation and analysis
-   **NumPy** --- numerical operations
-   **Matplotlib** --- visualization
-   **Seaborn** --- statistical visualization
-   **Scikit-learn** --- data standardization
-   **Google Colab** --- development environment
-   **GitHub** --- project hosting and version control

------------------------------------------------------------------------

## 📁 Project Structure

``` text
Global-Happiness-Report-Analysis/
│
├── data/
│   ├── 2015.csv
│   ├── 2016.csv
│   ├── 2017.csv
│   ├── 2018.csv
│   ├── 2019.csv
│   └── global_happiness_2015_2019_clean.csv
│
├── Global_Happiness_Report_Analysis.ipynb
├── README.md
├── requirements.txt
```

------------------------------------------------------------------------

## ▶️ How to Run

### Google Colab

1.  Open `Global_Happiness_Report_Analysis.ipynb` in Google Colab.
2.  Upload the World Happiness Report ZIP file when prompted.
3.  Run the notebook cells from top to bottom.
4.  The datasets will be extracted into the `data` folder.
5.  The analysis and visualizations will be generated automatically.

### Local Environment

Install the required libraries:

``` bash
pip install -r requirements.txt
```

Then open:

``` text
Global_Happiness_Report_Analysis.ipynb
```

with Jupyter Notebook, JupyterLab, or another compatible environment.

------------------------------------------------------------------------

## ⚠️ Limitations

-   The analysis covers only **2015--2019**.
-   Variable names and definitions changed across different report
    editions, so relevant variables were harmonized before combining the
    datasets.
-   One missing value was handled using median imputation.
-   The analysis focuses on relationships and comparisons rather than
    causal inference.
-   The dataset does not contain every social, cultural, political,
    demographic, or environmental factor that may influence happiness.

------------------------------------------------------------------------

## 🚀 Future Scope

-   Add more recent World Happiness Report data.
-   Perform regional and continental comparisons.
-   Create an interactive Power BI or Tableau dashboard.
-   Build an interactive country comparison tool.
-   Apply machine learning techniques for predictive analysis.
-   Study happiness trends over a longer time period.
-   Include additional socioeconomic and demographic variables.

------------------------------------------------------------------------

## 👨‍💻 Project Information

**Author:** Chand Khimani\
**Instructor:** Girish Gondaliya\
**Course:** BCA Data Analysis

------------------------------------------------------------------------

## 🌟 Final Note

This project demonstrates a complete **data analysis workflow**:

**Raw Data → Data Cleaning → Transformation → EDA → Visualization →
Correlation → Insights**

### 🌍 Turning Data Into Meaningful Insights 📊
