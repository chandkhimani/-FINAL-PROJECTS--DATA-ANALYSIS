<div align="center">

# 🚢 TITANIC SURVIVAL ANALYSIS
### **From Passenger Records → Survival Intelligence**

<p>
  <img src="https://img.shields.io/badge/Project-Data%20Analysis-0A66C2?style=for-the-badge">
  <img src="https://img.shields.io/badge/Domain-Exploratory%20Data%20Analysis-7B2CBF?style=for-the-badge">
  <img src="https://img.shields.io/badge/Python-3.x-F7C948?style=for-the-badge">
  <img src="https://img.shields.io/badge/Pandas-Data%20Wrangling-150458?style=for-the-badge">
  <img src="https://img.shields.io/badge/Seaborn-Visualization-2E8B57?style=for-the-badge">
  <img src="https://img.shields.io/badge/Status-Completed-success?style=for-the-badge">
</p>

**A professional Exploratory Data Analysis project that transforms the classic Titanic passenger dataset into a structured survival-intelligence study.**

> **Core idea:** Survival is not just a `0 / 1` column — it is a pattern hidden inside gender, class, age, fare, family structure, travel type, and embarkation.

</div>

---

## 🧭 PROJECT AT A GLANCE

| Dimension | Details |
|---|---|
| 🚢 Project | Titanic Survival Analysis |
| 🎯 Analysis Type | Exploratory Data Analysis (EDA) |
| 📦 Dataset | Titanic Passenger Dataset |
| 📊 Records | **891 passengers** |
| 🧩 Original Features | **12 columns** |
| 🛠️ Engineered Features | `CabinKnown`, `FamilySize`, `IsAlone`, `AgeGroup` |
| 🧹 Missing Age | **177 values** |
| 🛏️ Missing Cabin | **687 values (~77.10%)** |
| 🚢 Missing Embarked | **2 values** |
| ❤️ Overall Survival | **38.38%** |
| 👤 Survivors | **342** |
| ⚠️ Non-survivors | **549** |
| 🐍 Language | Python |
| 📓 Main Artifact | Jupyter / Google Colab Notebook |
| 👩‍💻 Author | **Chand Khimani** |
| 🎓 Program | **BCA Final Year** |
| 📚 Parallel Learning | **Data Analysis Course** |
| 👨‍🏫 Guide | **Prof. Girish Gondaliya Sir** |

---

# ✨ 01 — PROJECT VISION

This project is designed as a complete **EDA workflow**, not merely a collection of charts.

The analysis moves through a deliberate pipeline:

```text
RAW TITANIC DATA
      ↓
DATA UNDERSTANDING
      ↓
DATA QUALITY AUDIT
      ↓
MISSING-VALUE HANDLING
      ↓
FEATURE ENGINEERING
      ↓
EXPLORATORY ANALYSIS
      ↓
GROUP-WISE SURVIVAL ANALYSIS
      ↓
BIVARIATE ANALYSIS
      ↓
CORRELATION ANALYSIS
      ↓
AUTOMATED INSIGHT SUMMARY
      ↓
BUSINESS-STYLE INTERPRETATION
```

### 🎯 Project Objective

The objective is to discover **which passenger characteristics were associated with survival outcomes** and to demonstrate a complete, reproducible data-analysis workflow using Python.

---

# 🧠 02 — ANALYTICAL QUESTIONS

The notebook is structured around these questions:

1. What percentage of passengers survived?
2. Did females have a higher survival rate than males?
3. Which passenger class had the highest survival rate?
4. How was passenger age related to survival?
5. Did passengers paying higher fares have better survival outcomes?
6. Did travelling with family affect survival?
7. How did survival vary across embarkation ports?
8. Which numerical variables show stronger association with survival?

These questions turn the dataset into a **structured investigation** rather than a simple visualization exercise.

---

# 🗃️ 03 — DATASET PROFILE

The supplied Titanic dataset contains **891 passenger records** and **12 original columns**.

### Original Data Model

| Column | Meaning | Type / Role |
|---|---|---|
| `PassengerId` | Unique passenger identifier | Numeric ID |
| `Survived` | Survival outcome: 0 = No, 1 = Yes | Target |
| `Pclass` | Passenger class | Ordinal |
| `Name` | Passenger name | Text |
| `Sex` | Passenger gender | Categorical |
| `Age` | Passenger age | Numeric |
| `SibSp` | Siblings / spouses aboard | Numeric |
| `Parch` | Parents / children aboard | Numeric |
| `Ticket` | Ticket identifier | Text |
| `Fare` | Passenger fare | Numeric |
| `Cabin` | Cabin information | Text / Sparse |
| `Embarked` | Port of embarkation | Categorical |

---

# 🧬 04 — FEATURE ENGINEERING LAB

A major strength of this project is that the notebook does not rely only on raw columns.

It creates additional analytical features.

## `CabinKnown`

```python
df["CabinKnown"] = df["Cabin"].notna().astype(int)
```

Purpose:

- `1` → cabin information available
- `0` → cabin information missing

This converts a highly incomplete text field into an analyzable availability indicator.

---

## `FamilySize`

```python
df["FamilySize"] = df["SibSp"] + df["Parch"] + 1
```

Formula:

```text
FamilySize = SibSp + Parch + 1
```

The `+1` represents the passenger themselves.

---

## `IsAlone`

```python
df["IsAlone"] = np.where(
    df["FamilySize"] == 1,
    1,
    0
)
```

Interpretation:

| Value | Meaning |
|---:|---|
| `1` | Travelling alone |
| `0` | Travelling with family |

---

## `AgeGroup`

The notebook transforms age into four readable categories:

| Age | Group |
|---|---|
| `< 13` | Child |
| `13–19` | Teen |
| `20–59` | Adult |
| `60+` | Senior |

This makes age-based group comparison easier than relying only on raw ages.

---

# 🧹 05 — DATA QUALITY & CLEANING

The cleaning stage checks:

- missing values
- duplicate rows
- data types
- column availability
- numerical/categorical structure
- Cabin completeness
- Age completeness
- Embarked completeness

### Missing-value strategy

#### 🎂 Age
The notebook uses **median imputation**.

```python
age_median = df["Age"].median()
df["Age"] = df["Age"].fillna(age_median)
```

The original dataset contains **177 missing Age values**.

The median used by the dataset is:

> **28.00 years**

#### 🚢 Embarked
Missing `Embarked` values are handled using the **mode**, i.e. the most frequent category.

#### 🛏️ Cabin
Cabin has substantial missingness:

> **687 / 891 values ≈ 77.10% missing**

Instead of pretending the missing cabin values are known, the notebook creates `CabinKnown` to preserve the information about whether cabin data exists.

### 🔐 Data-quality philosophy

```text
Detect → Understand → Handle → Validate → Analyze
```

---

# 📊 06 — EDA ARCHITECTURE

The notebook progresses through multiple analytical layers.

### Layer 1 — Dataset Understanding
- head
- tail
- shape
- columns
- data types
- unique values
- descriptive statistics

### Layer 2 — Data Quality
- missing-value audit
- duplicate check
- data-type verification
- post-cleaning validation

### Layer 3 — Survival Analysis
- overall survival
- gender
- passenger class
- gender + class

### Layer 4 — Demographic Analysis
- age distribution
- age vs survival
- age groups
- gender distribution

### Layer 5 — Family & Travel Analysis
- family-size distribution
- family-size survival
- alone vs family

### Layer 6 — Economic & Geographic Analysis
- fare distribution
- fare vs survival
- embarkation distribution
- embarkation vs survival

### Layer 7 — Relationship Analysis
- bivariate plots
- correlation matrix
- survival correlation ranking

### Layer 8 — Automated Insight Engine
- overall summary
- gender insight
- class insight
- age-group insight
- family-size insight
- travel-type insight
- embarkation insight
- final key-insights table

---

# 📈 07 — VISUALIZATION GALLERY

The notebook includes a broad visualization portfolio.

| Visualization | Analytical Purpose |
|---|---|
| 📊 Count Plot | Passenger / survival counts |
| 📊 Bar Plot | Survival-rate comparison |
| 📉 Histogram | Distribution analysis |
| 📦 Box Plot | Distribution by survival status |
| 🔵 Scatter Plot | Relationship between numerical variables |
| 🔥 Heatmap | Correlation structure |
| 📈 KDE | Distribution shape |
| 🧩 Grouped Bar Chart | Multi-category comparison |

### Major visual analyses

```text
Overall Survival
      │
      ├── Gender
      │     ├── Survival Rate
      │     └── Survival Count
      │
      ├── Passenger Class
      │     ├── Survival Rate
      │     └── Survival Count
      │
      ├── Age
      │     ├── Distribution
      │     ├── Survival Distribution
      │     └── Age Groups
      │
      ├── Family
      │     ├── Family Size
      │     └── Alone vs Family
      │
      ├── Fare
      │     ├── Distribution
      │     └── Survival Comparison
      │
      └── Embarkation
            ├── Distribution
            └── Survival Rate
```

---

# 👩‍🦰 08 — GENDER SURVIVAL INTELLIGENCE

The dataset shows a substantial difference between male and female survival rates.

| Gender | Survival Rate |
|---|---:|
| **Female** | **74.20%** |
| Male | **18.89%** |

### 🔎 Interpretation

Female passengers in this dataset had a considerably higher observed survival rate than male passengers.

This is a **descriptive association**, not proof that gender alone caused the outcome.

---

# 🎫 09 — PASSENGER CLASS INTELLIGENCE

Survival also differs strongly across passenger classes.

| Passenger Class | Survival Rate |
|---:|---:|
| **1st Class** | **62.96%** |
| 2nd Class | **47.28%** |
| 3rd Class | **24.24%** |

### 🔎 Interpretation

The first-class group has the highest observed survival rate, while third class has the lowest.

This makes passenger class one of the most visually and statistically important categorical variables in the project.

---

# 👩‍🦰 + 🎫 10 — GENDER × CLASS

The notebook goes beyond single-variable analysis by combining:

```text
Passenger Class × Gender → Survival Rate
```

This is important because a passenger's survival outcome can be associated with multiple characteristics simultaneously.

The resulting grouped visualization gives a more detailed picture than looking at gender or class independently.

---

# 🎂 11 — AGE INTELLIGENCE

The notebook analyzes age in multiple ways:

- raw age distribution
- age vs survival
- age-group distribution
- age-group survival rate

### Observed age-group survival rates

| Age Group | Survival Rate |
|---|---:|
| **Child** | **57.97%** |
| Teen | **41.05%** |
| Adult | **36.52%** |
| Senior | **26.92%** |

### 🔎 Interpretation

Children show the highest observed survival rate among the engineered age groups, while seniors show the lowest.

Again, these are **group-level observations**, not causal conclusions.

---

# 👨‍👩‍👧 12 — FAMILY SIZE INTELLIGENCE

The notebook creates:

```text
FamilySize = SibSp + Parch + 1
```

and then evaluates survival rates across family-size groups.

Notable observed groups include:

| Family Size | Survival Rate |
|---:|---:|
| **4** | **72.41%** |
| 3 | **57.84%** |
| 2 | **55.28%** |
| 7 | **33.33%** |
| 1 | **30.35%** |

### ⚠️ Important analytical caution

Very large family-size groups can contain relatively few observations.

Therefore:

> A high percentage for a small group should not automatically be interpreted as a universally reliable pattern.

---

# 🧳 13 — ALONE vs FAMILY

The notebook creates an `IsAlone` feature and compares travel type.

| Travel Type | Survival Rate |
|---|---:|
| **With Family** | **50.56%** |
| Alone | **30.35%** |

### 🔎 Interpretation

Passengers travelling with family had a higher observed survival rate than passengers travelling alone in this dataset.

This is an association observed in the sample and may overlap with other variables such as age, gender, and passenger class.

---

# 💰 14 — FARE INTELLIGENCE

Fare is examined using:

- distribution analysis
- box plot by survival status
- average fare by survival
- fare-age-survival scatter plot

### Average fare

| Survival Status | Average Fare |
|---|---:|
| **Survived** | **48.40** |
| Did Not Survive | **22.12** |

### 🔎 Interpretation

Survivors paid a higher average fare in this dataset.

Fare may also act as an indirect indicator related to passenger class, so this relationship should not be interpreted in isolation.

---

# 🚢 15 — EMBARKATION INTELLIGENCE

The dataset contains three main embarkation codes:

| Code | Port |
|---|---|
| `C` | Cherbourg |
| `Q` | Queenstown |
| `S` | Southampton |

Observed survival rates:

| Port | Survival Rate |
|---|---:|
| **C** | **55.36%** |
| Q | **38.96%** |
| S | **33.90%** |

### 🔎 Interpretation

The observed survival rate differs across embarkation groups.

However, embarkation itself may be associated with passenger composition and class, so it should not be treated as an independent causal factor.

---

# 🔥 16 — CORRELATION INTELLIGENCE

The notebook calculates Pearson correlations for:

```text
Survived
Age
Fare
SibSp
Parch
FamilySize
Pclass
```

### Correlation with `Survived`

| Variable | Correlation |
|---|---:|
| **Fare** | **+0.257** |
| **Parch** | **+0.082** |
| **FamilySize** | **+0.017** |
| **SibSp** | **−0.035** |
| **Age** | **−0.065** |
| **Pclass** | **−0.338** |

### 🧠 Reading the result

- `Fare` has the strongest positive numerical association with survival among these variables.
- `Pclass` has the strongest negative association with survival.
- `FamilySize` has a correlation close to zero.
- `Age` has a weak negative linear correlation.

### ⚠️ Correlation ≠ Causation

A correlation value tells us about **association**, not direct cause.

For example:

```text
Correlation
    ↓
Association
    ≠
Causation
```

---

# 🧪 17 — STATISTICAL INTERPRETATION LAYER

The project demonstrates several important analytical principles.

### Descriptive statistics

Used to understand:

- central tendency
- spread
- minimum / maximum
- numerical distributions

### Grouped analysis

Used to compare survival across:

- gender
- class
- age groups
- family size
- travel type
- embarkation port

### Correlation analysis

Used to identify linear numerical associations.

### Visualization

Used to make patterns easier to identify and communicate.

---

# 🤖 18 — AUTOMATED INSIGHT ENGINE

One of the strongest structural elements of the notebook is the programmatic insight section.

Instead of manually writing every numerical conclusion, the notebook calculates:

```text
Overall Survival
       ↓
Gender Ranking
       ↓
Class Ranking
       ↓
Age-Group Ranking
       ↓
Family-Size Ranking
       ↓
Travel-Type Ranking
       ↓
Embarkation Ranking
       ↓
Correlation Ranking
       ↓
Final Key Insights Table
```

This makes the project more:

- reproducible
- scalable
- less dependent on hard-coded conclusions
- suitable for future datasets

---

# 🏆 19 — KEY DATA SNAPSHOT

<div align="center">

### 🚢 891
**Total Passengers**

### ❤️ 342
**Survivors**

### ⚠️ 549
**Non-Survivors**

### 📊 38.38%
**Overall Survival Rate**

### 👩 74.20%
**Female Survival Rate**

### 🎫 62.96%
**1st-Class Survival Rate**

### 💰 48.40
**Average Fare of Survivors**

### 🧳 50.56%
**With-Family Survival Rate**

</div>

---

# 🧩 20 — PROJECT ARCHITECTURE

```text
                         ┌─────────────────────┐
                         │ Titanic-Dataset.csv │
                         └──────────┬──────────┘
                                    │
                                    ▼
                         ┌─────────────────────┐
                         │ Data Loading        │
                         │ Pandas              │
                         └──────────┬──────────┘
                                    │
                                    ▼
                         ┌─────────────────────┐
                         │ Data Understanding  │
                         │ Shape / Types /     │
                         │ Statistics / Values │
                         └──────────┬──────────┘
                                    │
                                    ▼
                         ┌─────────────────────┐
                         │ Data Quality Audit  │
                         │ Missing / Duplicate │
                         └──────────┬──────────┘
                                    │
                                    ▼
                    ┌─────────────────────────────┐
                    │ Cleaning + Feature Creation  │
                    │ Age / Embarked / CabinKnown  │
                    │ FamilySize / IsAlone / AgeGroup│
                    └──────────────┬──────────────┘
                                   │
                                   ▼
                         ┌─────────────────────┐
                         │ Exploratory Analysis│
                         └──────────┬──────────┘
                                    │
             ┌──────────────────────┼──────────────────────┐
             ▼                      ▼                      ▼
        Demographics            Family/Travel          Fare/Port
             │                      │                      │
             └──────────────────────┼──────────────────────┘
                                    ▼
                         ┌─────────────────────┐
                         │ Correlation Analysis│
                         └──────────┬──────────┘
                                    │
                                    ▼
                         ┌─────────────────────┐
                         │ Insight Engine      │
                         └──────────┬──────────┘
                                    │
                                    ▼
                         ┌─────────────────────┐
                         │ Final Interpretation│
                         └─────────────────────┘
```

---

# 🛠️ 21 — TECH STACK

| Technology | Role |
|---|---|
| 🐍 Python | Core programming language |
| 🐼 Pandas | Data loading, cleaning, transformation |
| 🔢 NumPy | Numerical operations and feature creation |
| 📊 Matplotlib | Visualization foundation |
| 🎨 Seaborn | Statistical visualization |
| 📓 Jupyter / Google Colab | Notebook execution and presentation |
| 🗂️ CSV | Dataset format |

---

# 📁 22 — REPOSITORY STRUCTURE

Recommended GitHub structure:

```text
Titanic-Survival-Analysis/
│
├── 📓 Titanic_Survival_Analysis.ipynb
├── 📄 Titanic-Dataset.csv
├── 📘 README.md
│
└── 📂 docs/
    └── project-notes.md
```

> The `outputs/` and `docs/` folders are a recommended presentation structure; they are not additional files contained in the supplied notebook.

---

# ▶️ 23 — HOW TO RUN

## Option A — Google Colab

1. Open Google Colab.
2. Upload `Titanic_Survival_Analysis.ipynb`.
3. Upload `Titanic-Dataset.csv` when prompted by the notebook.
4. Run the notebook from top to bottom.
5. Review tables, visualizations, and insight outputs.

The notebook already contains an upload flow using:

```python
from google.colab import files
uploaded = files.upload()
```

---

## Option B — Jupyter Notebook

Install dependencies:

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

Launch:

```bash
jupyter notebook
```

Open:

```text
Titanic_Survival_Analysis.ipynb
```

Keep the CSV available in the working directory.

---

## Option C — VS Code

1. Install Python.
2. Install the VS Code Python/Jupyter extensions.
3. Open the project folder.
4. Open `Titanic_Survival_Analysis.ipynb`.
5. Select a Python kernel.
6. Run the cells sequentially.
7. Keep `Titanic-Dataset.csv` in the same project folder or upload it through the notebook's existing upload workflow.

---

# 📸 24 — SCREENSHOT / PRESENTATION CHECKLIST

For a professional academic submission, capture these outputs:

### 🥇 Must-Have Screenshots

- Dataset preview
- Dataset shape
- Missing-value report
- Cleaning result
- Overall survival chart
- Gender survival chart
- Passenger-class survival chart
- Gender + class chart
- Age distribution
- Age-group survival
- Family-size survival
- Alone vs family
- Fare distribution / survival comparison
- Embarkation survival
- Correlation heatmap
- Final key-insights table

### ⭐ Presentation Tip

Arrange screenshots in this order:

```text
Dataset → Cleaning → EDA → Comparison → Correlation → Insights
```

This creates a professional storytelling flow.

---

# 📚 25 — WHAT THIS PROJECT DEMONSTRATES

This project demonstrates practical skills in:

- Python programming
- Pandas DataFrame operations
- NumPy operations
- data loading
- data inspection
- missing-value handling
- duplicate detection
- descriptive statistics
- feature engineering
- categorical analysis
- numerical analysis
- groupby aggregation
- visualization
- correlation analysis
- interpretation of EDA results
- automated insight generation
- data storytelling

---

# ⚠️ 26 — LIMITATIONS

This project intentionally remains an **Exploratory Data Analysis and Visualization** project.

### Key limitations

1. The Titanic dataset represents a single historical event.
2. Results cannot automatically be generalized to all disasters or populations.
3. Age contains missing values and is handled using median imputation.
4. Cabin has very high missingness.
5. Median-imputed ages are estimates, not original observations.
6. Some survival patterns may be influenced by multiple interacting variables.
7. Correlation does not prove causation.
8. Simple EDA cannot explain every underlying mechanism.
9. The project does not currently build a predictive machine-learning model.
10. Historical data may contain limitations or biases affecting interpretation.

---

# 🚀 27 — FUTURE SCOPE

This project can evolve from **EDA → Predictive Analytics → Decision Intelligence**.

## 🤖 Phase 1 — Machine Learning

Possible classification models:

```text
Logistic Regression
Decision Tree
Random Forest
K-Nearest Neighbors
```

Target:

```text
Survived
```

---

## 🧬 Phase 2 — Advanced Feature Engineering

Potential additions:

- passenger title extraction from `Name`
- ticket group size
- cabin deck extraction
- family categories
- child/adult indicators
- family survival features
- ticket-sharing patterns

---

## 📊 Phase 3 — Interactive Dashboard

Possible tools:

- Power BI
- Tableau
- Plotly

Dashboard pages could include:

```text
Overview
   ↓
Demographics
   ↓
Class & Fare
   ↓
Family & Travel
   ↓
Survival Drivers
   ↓
Interactive Filters
```

---

## 🧠 Phase 4 — Explainable Prediction

A future ML version could answer:

> “Why does this passenger have a higher or lower predicted survival probability?”

Possible additions:

- feature importance
- confusion matrix
- precision / recall
- F1-score
- ROC-AUC
- SHAP-based explainability

---

# 💎 28 — WHY THIS PROJECT IS STRONG

The project is valuable because it follows a **complete analytical lifecycle**:

```text
RAW DATA
   ↓
QUALITY CHECK
   ↓
CLEAN DATA
   ↓
ENGINEERED FEATURES
   ↓
EDA
   ↓
VISUAL STORY
   ↓
STATISTICAL ASSOCIATION
   ↓
AUTOMATED INSIGHTS
   ↓
CONCLUSION
```

It demonstrates that data analysis is not simply:

> “Make a graph.”

Instead, it is:

> **Question → Data → Quality → Transformation → Analysis → Evidence → Interpretation**

---

# 🎓 29 — ACADEMIC VALUE

### Why this project is suitable for a BCA / Data Analysis portfolio

It demonstrates the ability to:

- work with a real-world dataset
- identify data-quality issues
- transform raw variables
- build meaningful derived features
- compare categorical groups
- visualize distributions
- evaluate relationships
- communicate findings
- maintain reproducible analysis

This makes it suitable as a **Data Analysis course project, GitHub portfolio project, or academic practical submission**.

---

# 🧠 30 — FINAL TAKEAWAYS

### Finding 01 — Gender
Female passengers had a much higher observed survival rate than male passengers.

### Finding 02 — Passenger Class
First-class passengers had the highest observed survival rate, while third-class passengers had the lowest.

### Finding 03 — Age
The engineered Child group had the highest observed age-group survival rate.

### Finding 04 — Family
Passengers travelling with family showed a higher observed survival rate than those travelling alone.

### Finding 05 — Fare
Survivors paid a substantially higher average fare than non-survivors.

### Finding 06 — Embarkation
Survival rates varied across embarkation groups.

### Finding 07 — Numerical Association
Fare showed the strongest positive correlation with `Survived` among the selected numerical variables, while `Pclass` showed the strongest negative correlation.

### Finding 08 — Statistical Discipline
These findings describe associations in the dataset and **do not establish causation**.

---

# 🏁 CONCLUSION

The **Titanic Survival Analysis** project presents a complete Exploratory Data Analysis workflow using Python.

Starting with **891 passenger records**, the project performs data inspection, quality checks, missing-value treatment, feature engineering, visualization, group-based survival analysis, bivariate analysis, and correlation analysis.

The analysis reveals strong differences in observed survival outcomes across passenger gender and class, while additional patterns emerge through age, family structure, fare, and embarkation analysis.

Most importantly, the project demonstrates a professional analytical mindset:

> **Clean the data.  
> Engineer useful features.  
> Ask meaningful questions.  
> Visualize the evidence.  
> Quantify the relationships.  
> Interpret carefully.  
> Never confuse correlation with causation.**

---

# 👩‍💻 AUTHOR

<div align="center">

## **CHAND KHIMANI**

**BCA Final Year**  
**Data Analysis Course**

### Guided By
**Prof. Girish Gondaliya Sir**

---

### 🚢 Titanic Survival Analysis
**Turning Passenger Data into Survival Intelligence**

⭐ If this project helps you, consider giving the repository a star.

</div>

---

# 📜 PROJECT STATUS

```text
╔════════════════════════════════════════════════|
║              TITANIC SURVIVAL ANALYSIS        |  
╠═══════════════════════════════════════════════╣
║ Data Loading                        ✅        ║ 
║ Data Understanding                  ✅        ║
║ Data Quality Audit                  ✅        ║
║ Missing Value Handling              ✅        ║
║ Feature Engineering                 ✅        ║
║ Exploratory Data Analysis           ✅        
║ Survival Analysis                   ✅        ║
║ Family / Travel Analysis            ✅        ║
║ Fare / Embarkation Analysis         ✅        ║
║ Correlation Analysis                ✅        ║
║ Automated Insight Engine            ✅        ║
║ Conclusion                          ✅        ║
║ Future Scope                        🚀        ║
╚═══════════════════════════════════════════════╝
```

---

<div align="center">

### 🚢 **DATA → PATTERNS → INSIGHTS → INTELLIGENCE**

**Built with Python • Pandas • NumPy • Matplotlib • Seaborn**

**© Chand Khimani — Titanic Survival Analysis**

</div>
