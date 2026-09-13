# ◈ FINAL DATA ANALYSIS PROJECTS
## Five Real-World Problems • One Analytical Journey

<p align="center">
  <b>Python Data Analysis & Visualization Portfolio</b><br>
  Pandas • NumPy • Matplotlib • Seaborn • Plotly
</p>

---

## ✦ Repository Overview

Welcome to **Final Data Analysis Projects** — a collection of five independent Data Analysis projects developed as part of an academic learning journey.

Each project uses a real-world dataset to answer a different analytical question. Together, the projects demonstrate the complete data-analysis workflow:

> **Raw Data → Inspection → Cleaning → EDA → Analysis → Visualization → Insights**

### The Five Projects

| # | Project | Domain | Main Focus |
|---|---|---|---|
| 01 | 🦠 COVID-19 Visualization Data Analysis | Public Health | Cases, deaths, recoveries & interventions |
| 02 | 🌍 Global Happiness Report Analysis | Social & Economic | Happiness and contributing factors |
| 03 | 🚢 Titanic Survival Analysis | Historical / EDA | Factors associated with survival |
| 04 | 🌫️ Air Quality Analysis | Environment | Pollution trends & relationships |
| 05 | 📈 Stock Market Analysis | Finance | Price trends, moving averages & volume |

---

# ◇ REPOSITORY ARCHITECTURE

```text
Final-Data-Analysis-Projects/
│
├── 01_COVID-19-Visualization/
│   ├── COVID-19 Visualization Data Analysis.ipynb
│   ├── covid_data.csv
│   └── README.md
│
├── 02_Global-Happiness-Report-Analysis/
│   ├── Global Happiness Report Analysis.ipynb
│   ├── happiness_data.csv
│   └── README.md
│
├── 03_Titanic-Survival-Analysis/
│   ├── Titanic Survival Analysis.ipynb
│   ├── titanic.csv
│   └── README.md
│
├── 04_Air-Quality-Analysis/
│   ├── Air Quality Analysis.ipynb
│   ├── air_quality.csv
│   └── README.md
│
├── 05_Stock-Market-Analysis/
│   ├── Stock Market Analysis.ipynb
│   ├── stock_market.csv
│   └── README.md
│
└── README.md
```

### Why this structure?

Every project is kept **self-contained**. Its notebook, dataset and project-specific documentation remain together, while this root README provides a single professional overview of the complete repository.

---

# 01 ┃ 🦠 COVID-19 VISUALIZATION DATA ANALYSIS

### Pandemic Data → Trends → Intervention Analysis

**Objective**

Analyze the spread of COVID-19 over time and examine trends in cases, recoveries and deaths across countries, while visualizing government containment and health intervention trends.

**Dataset**

- Our World in Data COVID-19 Dataset
- Historical Johns Hopkins University CSSE recovery data

**Tools**

`Pandas` `NumPy` `Matplotlib` `Seaborn` `Plotly`

**Core Analysis**

- Dataset inspection and validation
- Data cleaning and date processing
- COVID-19 case trends
- Death trends
- Country comparison
- Historical recovery analysis
- Heatmap analysis
- Interactive Plotly visualization
- India government intervention vs reported case trends

**Analytical Principle**

The intervention comparison is descriptive. It highlights patterns occurring over time and does not claim that government measures alone caused changes in reported cases.

---

# 02 ┃ 🌍 GLOBAL HAPPINESS REPORT ANALYSIS

### Happiness Score → Economic & Social Factors

**Objective**

Analyze World Happiness Report data to understand factors associated with happiness across different countries.

**Dataset**

World Happiness Report Dataset — Kaggle

**Key Variables**

- Happiness / Life Ladder score
- GDP per capita
- Social support
- Healthy life expectancy

**Tools**

`Pandas` `Matplotlib` `Seaborn`

**Core Analysis**

- Data cleaning and preparation
- Happiness distribution
- Country-level comparison
- Happiness vs GDP
- Happiness vs social support
- Happiness vs life expectancy
- Correlation heatmap

**Analytical Principle**

Correlation represents an association between variables; it does not by itself prove that one factor directly causes happiness.

---

# 03 ┃ 🚢 TITANIC SURVIVAL ANALYSIS

### Passenger Data → EDA → Survival Patterns

**Objective**

Perform exploratory data analysis on the Titanic dataset to understand passenger characteristics associated with survival.

**Dataset**

Titanic Dataset — Kaggle

**Key Variables**

- Survival
- Passenger class
- Gender
- Age
- Fare
- Family-related variables

**Tools**

`Pandas` `Matplotlib` `Seaborn`

**Core Analysis**

- Dataset inspection
- Missing-value analysis
- Data cleaning
- Overall survival distribution
- Survival by passenger class
- Survival by gender
- Survival by age
- Class and gender comparison
- Fare and passenger-distribution analysis

---

# 04 ┃ 🌫️ AIR QUALITY ANALYSIS

### Pollution Data → Time → Environmental Patterns

**Objective**

Analyze air-quality data from different locations to understand pollution levels over time and explore relationships with available weather/environmental variables.

**Dataset Options**

- UCI Machine Learning Repository Air Quality Dataset
- OpenAQ Global Air Quality Data

**Tools**

`Pandas` `Matplotlib` `Seaborn`

**Core Analysis**

- Data preparation
- Pollution trends over time
- Location-based comparison
- Pollutant distributions
- Pollutant relationships
- Correlation heatmap
- Relationship between pollution and available weather variables

**Analytical Principle**

Observed relationships depend on the selected dataset, available variables and measurement locations.

---

# 05 ┃ 📈 STOCK MARKET ANALYSIS

### Price History → Trend → Moving Average → Volume

**Objective**

Analyze historical stock-market data to identify trends and patterns in stock prices over time.

**Dataset**

Yahoo Finance historical data through `yfinance` or a suitable Kaggle stock dataset.

**Key Variables**

- Date
- Open
- High
- Low
- Close
- Adjusted Close
- Trading Volume

**Tools**

`Pandas` `NumPy` `Matplotlib` `Seaborn`

**Core Analysis**

- Historical closing-price trend
- Daily price movement
- High/low range
- Moving-average analysis
- Trading-volume trend
- Price and volume relationship

**Analytical Principle**

Historical price patterns and indicators are descriptive analytical tools and cannot guarantee future market performance.

---

# ◈ THE COMMON ANALYTICAL ENGINE

Although the five datasets belong to different domains, the projects share the same analytical foundation:

```text
                 ┌─────────────────────┐
                 │      RAW DATA       │
                 └──────────┬──────────┘
                            ↓
                 ┌─────────────────────┐
                 │ DATA INSPECTION     │
                 │ Shape • Columns     │
                 │ Types • Missingness │
                 └──────────┬──────────┘
                            ↓
                 ┌─────────────────────┐
                 │ DATA CLEANING       │
                 │ Validation • Dates  │
                 │ Missing Values      │
                 └──────────┬──────────┘
                            ↓
                 ┌─────────────────────┐
                 │ EDA                 │
                 │ Distributions       │
                 │ Groups • Trends     │
                 └──────────┬──────────┘
                            ↓
                 ┌─────────────────────┐
                 │ ANALYSIS            │
                 │ Comparisons         │
                 │ Relationships       │
                 └──────────┬──────────┘
                            ↓
                 ┌─────────────────────┐
                 │ VISUALIZATION       │
                 │ Matplotlib/Seaborn  │
                 │ Plotly where used   │
                 └──────────┬──────────┘
                            ↓
                 ┌─────────────────────┐
                 │ INSIGHTS &          │
                 │ CONCLUSION          │
                 └─────────────────────┘
```

---

# ◇ TECHNOLOGY MATRIX

| Project | Pandas | NumPy | Matplotlib | Seaborn | Plotly |
|---|:---:|:---:|:---:|:---:|:---:|
| 🦠 COVID-19 | ✓ | ✓ | ✓ | ✓ | ✓ |
| 🌍 Happiness | ✓ | — | ✓ | ✓ | — |
| 🚢 Titanic | ✓ | — | ✓ | ✓ | — |
| 🌫️ Air Quality | ✓ | — | ✓ | ✓ | — |
| 📈 Stock Market | ✓ | ✓ | ✓ | ✓ | — |

**Note:** The matrix follows the libraries specified for each assignment. Libraries are used according to the analytical requirement of each project.

---

# ◇ WHAT THIS REPOSITORY DEMONSTRATES

## Data Handling

- Reading structured datasets
- Inspecting rows and columns
- Selecting relevant fields
- Filtering and sorting
- GroupBy-based analysis

## Data Cleaning

- Missing-value inspection
- Data-type conversion
- Date/time processing
- Handling incomplete records
- Basic data validation

## Exploratory Data Analysis

- Descriptive summaries
- Distributions
- Category comparisons
- Time-series analysis
- Correlation analysis

## Visualization

- Line charts
- Bar charts
- Histograms
- Scatter plots
- Heatmaps
- Comparative visualizations
- Interactive Plotly charts

## Analytical Thinking

- Identifying trends
- Comparing categories
- Comparing countries/locations
- Studying variable relationships
- Converting observations into findings
- Recognizing dataset limitations

---

# ◇ PROJECT-BY-PROJECT QUESTIONS

| Project | Question Being Investigated |
|---|---|
| 🦠 COVID-19 | How did COVID-19 cases, deaths and recoveries change over time, and what intervention patterns can be observed? |
| 🌍 Happiness | Which economic, social and health-related variables are associated with happiness? |
| 🚢 Titanic | Which passenger characteristics were associated with different survival outcomes? |
| 🌫️ Air Quality | How did pollution levels change across time/locations and how were pollutants related? |
| 📈 Stock Market | What trends and patterns can be observed in historical prices, moving averages and trading volume? |

---

# ◇ QUALITY CONTROL CHECKLIST

Before submission, each project should satisfy:

```text
✓ Correct dataset included
✓ Notebook opens correctly
✓ Required libraries imported
✓ Dataset loaded successfully
✓ Dataset structure inspected
✓ Missing values checked
✓ Data cleaned where necessary
✓ Assignment objectives addressed
✓ Appropriate charts created
✓ Chart titles included
✓ X-axis / Y-axis labels included
✓ Findings explained
✓ Conclusion included
✓ Project README included
✓ Files named clearly
✓ GitHub folder structure organized
```

---

# ⚠️ DATA INTERPRETATION & LIMITATIONS

Good data analysis is not only about producing attractive charts; it is also about understanding what the data can and cannot prove.

Therefore:

- **Correlation ≠ causation.**
- Reported values may not represent the complete real-world situation.
- Missing data can affect results.
- Different countries or locations may use different reporting/measurement methods.
- Historical datasets may contain revisions or inconsistencies.
- Financial indicators describe historical behavior and do not guarantee future performance.
- Conclusions should remain within the evidence provided by the selected dataset.

---

# ◇ HOW TO EXPLORE THIS REPOSITORY

### 01 — Choose a Project

Open one of the five numbered project folders.

### 02 — Read Its README

Each project has its own documentation with project-specific details.

### 03 — Open the Notebook

Launch the `.ipynb` file and run the analysis.

### 04 — Explore the Dataset

The corresponding `.csv` file is stored with the project where applicable.

### 05 — Review the Findings

Move to the final analysis/finding sections to understand what the data reveals.

---

# ◇ WHY FIVE PROJECTS?

The five projects cover different real-world domains:

```text
🦠 PUBLIC HEALTH
      ↓
🌍 SOCIAL & ECONOMIC WELL-BEING
      ↓
🚢 HISTORICAL HUMAN DATA
      ↓
🌫️ ENVIRONMENT
      ↓
📈 FINANCE
```

This variety demonstrates that the same fundamental data-analysis skills can be applied to very different datasets and questions.

---

# 🎓 ACADEMIC INFORMATION

**Developer:** Chand Khimani  
**Academic Status:** BCA Final Year Student  
**Course:** Data Analysis  
**Guided By:** Girish Gondaliya Sir

This repository has been prepared as a multi-project academic Data Analysis submission.

---

# ◇ PROJECT STATUS

| Project | Status |
|---|---|
| 🦠 COVID-19 Visualization | ✅ Completed |
| 🌍 Global Happiness Report | 🔄 In Progress / Update |
| 🚢 Titanic Survival Analysis | 🔄 In Progress / Update |
| 🌫️ Air Quality Analysis | 🔄 In Progress / Update |
| 📈 Stock Market Analysis | 🔄 In Progress / Update |

> Update the status of each project to **Completed** after its notebook has been fully tested.

---

# ✦ THE FINAL IDEA

Five projects.  
Five datasets.  
Five real-world domains.  
One analytical mindset.

```text
DATA
 ↓
UNDERSTAND
 ↓
CLEAN
 ↓
ANALYZE
 ↓
VISUALIZE
 ↓
EXPLAIN
```

<p align="center">
  <b>✨ DATA HAS A STORY. ANALYSIS REVEALS IT. ✨</b>
  <br><br>
  <i>Built with Python • Data Analysis • Visualization</i>
  <br><br>
  ⭐ Thank you for exploring this repository. ⭐
</p>
