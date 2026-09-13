# 🚢 Titanic Survival Analysis

### Understanding the Factors That Influenced Passenger Survival

---

## 📌 Project Overview

The **Titanic Survival Analysis** project performs Exploratory Data Analysis (EDA) on the Titanic passenger dataset to understand the factors associated with passenger survival.

The analysis explores important passenger characteristics such as gender, passenger class, age, fare, family size, travelling status, and embarkation port.

This project demonstrates a complete beginner-friendly data analysis workflow using Python, Pandas, NumPy, Matplotlib, and Seaborn.

---

## 🎯 Objectives

The main objectives of this project are:

- Analyze the overall passenger survival rate.
- Compare survival rates between male and female passengers.
- Analyze survival rates across different passenger classes.
- Examine the relationship between age and survival.
- Investigate the relationship between fare and survival.
- Analyze the effect of family size on survival.
- Compare passengers travelling alone with passengers travelling with family.
- Analyze survival rates based on embarkation port.
- Identify important patterns and relationships in the dataset.
- Present findings through clear and meaningful visualizations.

---

## ❓ Analytical Questions

This project attempts to answer the following questions:

1. What percentage of Titanic passengers survived?
2. Did female passengers have a higher survival rate than male passengers?
3. Which passenger class had the highest survival rate?
4. How was age associated with survival?
5. Did passengers paying higher fares show different survival patterns?
6. Did family size influence survival?
7. Was travelling alone associated with a different survival rate?
8. Did survival rates differ across embarkation ports?
9. Which numerical variables showed stronger associations with survival?
10. What major patterns can be observed from the Titanic dataset?

---

## 📊 Dataset

The project uses the **Titanic passenger dataset**.

The dataset contains passenger information such as:

- Passenger class
- Gender
- Age
- Number of siblings/spouses aboard
- Number of parents/children aboard
- Passenger fare
- Cabin information
- Embarkation port
- Survival status

The dataset is inspected before analysis so that the notebook works with the actual available columns and values.

---

## 🛠️ Technologies Used

- **Python**
- **Google Colab**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **GitHub**

---

## 📚 Libraries Used

The project uses the following Python libraries:

```text
pandas
numpy
matplotlib
seaborn
```

---

## 🧹 Data Cleaning

The following data-cleaning steps were performed:

- Checked dataset dimensions.
- Inspected column names and data types.
- Checked missing values.
- Checked duplicate records.
- Handled missing `Age` values using median imputation.
- Handled missing `Embarked` values using the mode.
- Inspected missing values in `Cabin`.
- Created a `CabinKnown` indicator.
- Verified missing values and duplicate records after cleaning.

The cleaning process was designed to avoid unnecessarily removing large portions of the dataset.

---

## 🔄 Feature Engineering

Additional features were created to make the analysis more meaningful.

### FamilySize

```text
FamilySize = SibSp + Parch + 1
```

This represents the passenger's total family/travelling group size.

### IsAlone

Passengers were classified as:

- **Alone**
- **With Family**

based on their `FamilySize`.

### AgeGroup

Passengers were grouped into:

- **Child**
- **Teen**
- **Adult**
- **Senior**

These features help compare survival patterns across different passenger groups.

---

## 📊 Exploratory Data Analysis

The project includes analysis of the following areas:

### 🚢 Overall Survival

The total number and percentage of passengers who survived and did not survive were calculated.

### 👩 Gender Analysis

Survival rates were compared between male and female passengers.

### 🎫 Passenger Class Analysis

Survival rates were analyzed across different passenger classes.

### 👩‍🦰 Gender + Class Analysis

The combined relationship between gender, passenger class, and survival was examined.

### 🎂 Age Analysis

Age distribution and survival patterns across different age groups were explored.

### 👨‍👩‍👧 Family Analysis

Family size and travelling-alone status were analyzed in relation to survival.

### 💰 Fare Analysis

Fare distributions and average fares were compared between survival groups.

### 🚢 Embarkation Analysis

Survival rates were compared across the available embarkation ports.

---

## 📈 Visualizations

The project includes visualizations directly inside the Google Colab/Jupyter Notebook.

Visualizations include:

- Count plots
- Bar charts
- Histograms
- Box plots
- Grouped bar charts
- Scatter plots
- Correlation heatmap

Each visualization is used to help identify meaningful patterns in the dataset.

---

## 🔥 Correlation Analysis

A correlation matrix was created using meaningful numerical variables, including:

- `Survived`
- `Age`
- `Fare`
- `SibSp`
- `Parch`
- `FamilySize`
- `Pclass`

The correlation heatmap helps identify numerical associations between variables.

> **Important:** Correlation indicates association between variables and does not prove causation.

---

## 🔍 Key Findings

The analysis identifies survival patterns across several passenger characteristics.

The major factors examined include:

- Gender
- Passenger class
- Age group
- Family size
- Travelling status
- Fare
- Embarkation port

The exact survival percentages and group comparisons are calculated directly from the dataset in the notebook rather than being manually entered.

---

## ⚠️ Limitations

This analysis has several limitations:

1. The Titanic dataset represents a single historical event.
2. Missing information exists in some variables.
3. Median imputation for Age may not represent the actual ages of passengers with missing values.
4. Cabin information contains substantial missingness.
5. Exploratory analysis cannot explain every possible factor affecting survival.
6. Correlation does not establish causation.
7. The project focuses on EDA rather than predictive machine learning.
8. Historical data may contain limitations or biases.

---

## 🏁 Conclusion

The Titanic Survival Analysis project demonstrates how Exploratory Data Analysis can be used to investigate patterns in a real-world dataset.

The project covers the complete basic EDA workflow:

**Data Loading → Data Understanding → Data Cleaning → Feature Engineering → Exploratory Analysis → Visualization → Correlation Analysis → Findings**

The analysis provides practical experience with Python, Pandas, Matplotlib, and Seaborn while developing an understanding of how different passenger characteristics were associated with survival.

---

## 🚀 Future Scope

This project can be extended in several ways.

### 🤖 Machine Learning

Classification models such as:

- Logistic Regression
- Decision Tree
- Random Forest
- K-Nearest Neighbors

can be used to predict passenger survival.

### 🔄 Advanced Feature Engineering

Additional features could be created from passenger information, such as:

- Passenger titles
- Ticket group size
- Cabin deck
- More detailed family categories

### 📊 Statistical Analysis

Statistical tests could be performed to determine whether observed differences between passenger groups are statistically significant.

### 📈 Interactive Dashboard

The analysis could be converted into an interactive dashboard using:

- Power BI
- Tableau
- Plotly

### 🧠 Predictive Analytics

Machine learning models could be evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

---

## ▶️ How to Run the Project

### Option 1 — Google Colab

1. Open Google Colab.
2. Upload `Titanic_Survival_Analysis.ipynb`.
3. Upload the Titanic CSV dataset when requested.
4. Run the notebook cells from top to bottom.

### Option 2 — Local Python Environment

Install the required libraries:

```bash
pip install -r requirements.txt
```

Then open the notebook using Jupyter Notebook, JupyterLab, or another compatible notebook environment.

---

## 📁 Project Structure

```text
Project-3-Titanic-Survival-Analysis/
│
├── Titanic_Survival_Analysis.ipynb
├── README.md
├── requirements.txt
│
└── data/
    └── Titanic-Dataset.csv
```

---

## 👨‍💻 Project Information

**Author:** Chand Khimani  
**Instructor:** Girish Gondaliya  
**Course:** BCA Data Analysis

---

## ⭐ Project Highlights

- Beginner-friendly Python implementation
- Complete Exploratory Data Analysis workflow
- Data cleaning and feature engineering
- Survival rate analysis
- Gender and passenger class analysis
- Age and fare analysis
- Family and travel analysis
- Embarkation analysis
- Correlation analysis
- Multiple data visualizations
- GitHub-ready project structure
- Suitable for academic submission and portfolio presentation

---

## 📌 Note

This project is intended for educational and analytical purposes.
