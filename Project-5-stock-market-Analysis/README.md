# 📈 Stock Market Analysis

### Historical Stock Price Trends, Moving Averages & Trading Activity

[![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python\&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas\&logoColor=white)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/NumPy-Numerical%20Computing-013243?logo=numpy\&logoColor=white)](https://numpy.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange)](https://matplotlib.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-Statistical%20Visualization-4C72B0)](https://seaborn.pydata.org/)
[![Google Colab](https://img.shields.io/badge/Google%20Colab-Notebook-F9AB00?logo=googlecolab\&logoColor=white)](https://colab.research.google.com/)

---

## 📌 Project Overview

**Stock Market Analysis** is a Python-based data analysis project focused on exploring historical stock market data to identify trends, patterns, price movements, trading activity, and volatility.

The project uses historical stock price information containing **Open, High, Low, Close, Adjusted Close, and Volume** values.

Through data analysis and visualization techniques, the project provides a clear understanding of how stock prices and trading activity changed over the analyzed period.

---

## 🎯 Project Objective

The main objective of this project is to analyze historical stock market data and identify meaningful patterns and trends in stock prices over time.

The analysis focuses on:

* 📈 Understanding historical price trends
* 📊 Analyzing closing prices
* 🔄 Calculating moving averages
* 📦 Studying trading volume
* ⚡ Measuring daily returns and volatility
* 🔍 Examining the relationship between price and volume
* 🏆 Identifying the best and worst trading days
* 🔗 Analyzing correlations between stock indicators
* 📋 Summarizing overall stock performance

> **Note:** This project focuses on historical data analysis and visualization. It does not predict future stock prices or provide financial advice.

---

## 🗂️ Dataset

The project uses a historical stock market dataset stored in CSV format.

### Dataset Features

| Column      | Description                          |
| ----------- | ------------------------------------ |
| `Date`      | Trading date                         |
| `Open`      | Opening stock price                  |
| `High`      | Highest price during the trading day |
| `Low`       | Lowest price during the trading day  |
| `Close`     | Closing stock price                  |
| `Adj Close` | Adjusted closing price               |
| `Volume`    | Number of shares traded              |

The dataset is analyzed using **Pandas** after being loaded into the Google Colab environment.

---

## 🛠️ Technologies & Libraries

### Programming Language

* **Python**

### Data Analysis

* **Pandas** — Data loading, cleaning, manipulation, and statistical analysis
* **NumPy** — Numerical calculations

### Data Visualization

* **Matplotlib** — Price, volume, return, and trend visualizations
* **Seaborn** — Correlation heatmap and statistical visualization

### Development Environment

* **Google Colab**
* **GitHub**

---

## 🔍 Analysis Performed

### 1. Dataset Exploration

The dataset was initially explored to understand:

* Number of records
* Number of columns
* Available features
* Data types
* Date range
* Initial records

---

### 2. Data Quality Check

The dataset was checked for:

* Missing values
* Duplicate records
* Duplicate dates
* Data consistency

Duplicate records were removed when necessary.

---

### 3. Descriptive Statistics

Statistical analysis was performed on the major numerical indicators.

The analysis includes:

* Mean
* Median
* Minimum
* Maximum
* Standard deviation
* Range

This provides an overall statistical understanding of stock prices and trading volume.

---

### 4. Closing Price Trend Analysis

The historical **Closing Price** was visualized over time to understand the overall stock price movement.

This visualization helps identify:

* Upward trends
* Downward trends
* Major price movements
* Periods of higher volatility

---

### 5. Moving Average Analysis

Two moving averages were calculated:

* **20-Day Moving Average**
* **50-Day Moving Average**

Moving averages smooth short-term price fluctuations and help identify the underlying price trend.

The project compares the moving averages with the actual closing price.

---

### 6. Trading Volume Analysis

Trading volume was analyzed to understand market activity.

The project identifies:

* Average trading volume
* Highest trading volume
* Date of highest trading activity
* Changes in market participation over time

---

### 7. Daily Returns Analysis

Daily percentage returns were calculated using closing prices.

The analysis measures:

* Average daily return
* Highest daily return
* Lowest daily return
* Daily volatility

Daily returns provide insight into short-term stock price movements.

---

### 8. Price & Volume Relationship

The relationship between **Closing Price** and **Trading Volume** was examined using correlation analysis.

This helps determine whether price and trading activity tend to move together.

---

### 9. Best & Worst Trading Days

The project identifies:

🏆 **Best Trading Day**
The day with the highest daily percentage return.

📉 **Worst Trading Day**
The day with the lowest daily percentage return.

This provides a quick view of the most significant positive and negative daily movements.

---

### 10. Overall Stock Performance

The project's overall performance analysis compares:

* Starting closing price
* Ending closing price
* Total price change
* Overall percentage return
* General price direction

The analysis classifies the historical trend as:

* 📈 Upward
* 📉 Downward
* ➡️ Stable

---

### 11. Correlation Analysis

A correlation matrix was created to examine relationships among:

* Open
* High
* Low
* Close
* Adjusted Close
* Volume
* Daily Return

A heatmap is used to make these relationships easier to understand visually.

---

## 📊 Visualizations

The project contains multiple visualizations designed to communicate the analysis clearly.

### 📈 Closing Price Trend

Shows how the stock's closing price changed over the analyzed period.

### 📊 Moving Average Chart

Compares:

* Closing Price
* 20-Day Moving Average
* 50-Day Moving Average

### 📦 Trading Volume Chart

Shows daily trading volume and its relationship with average market activity.

### 📈 Daily Returns Chart

Displays positive and negative daily stock returns.

### 📊 Price & Volume Comparison

Compares stock price movements with trading activity.

### 🔗 Correlation Heatmap

Visualizes the relationships between numerical stock market indicators.

---

## 💡 Key Insights

The analysis provides insights into:

* The overall historical direction of the stock
* Changes in closing prices over time
* Short-term and medium-term price trends
* Periods of high trading activity
* Daily gains and losses
* Stock price volatility
* Relationships between market indicators
* Strongest positive and negative trading days

The final notebook automatically generates the major findings from the analyzed dataset.

---

## 📁 Project Structure

```text
Stock-Market-Analysis/
│
├── Stock_Market_Analysis.ipynb
├── stock_data.csv
├── README.md
└── requirements.txt
```

### File Description

| File                          | Purpose                                           |
| ----------------------------- | ------------------------------------------------- |
| `Stock_Market_Analysis.ipynb` | Complete Python analysis and visualizations       |
| `stock_data.csv`              | Historical stock market dataset used for analysis |
| `README.md`                   | Project documentation                             |
| `requirements.txt`            | Required Python libraries                         |

---

## 🚀 How to Run the Project

### Option 1 — Google Colab

1. Open **Google Colab**.
2. Upload `Stock_Market_Analysis.ipynb`.
3. Run the notebook cells in order.
4. When prompted, upload `stock_data.csv`.
5. Execute all analysis and visualization cells.
6. Review the generated insights and conclusion.

### Option 2 — Local Python Environment

Clone or download the project repository.

Install the required libraries:

```bash
pip install -r requirements.txt
```

Then open:

```text
Stock_Market_Analysis.ipynb
```

using Jupyter Notebook, JupyterLab, or another compatible environment.

---

## 📦 Requirements

The project uses the following Python libraries:

```text
pandas
numpy
matplotlib
seaborn
```

---

## 🎓 Learning Outcomes

Through this project, the following Data Analysis concepts are demonstrated:

* Data loading using Pandas
* Data cleaning
* Missing-value checking
* Duplicate detection
* Data exploration
* Descriptive statistics
* Date-time handling
* Rolling calculations
* Percentage-change calculations
* Correlation analysis
* Data visualization
* Trend analysis
* Interpretation of analytical results

---

## 🔮 Future Improvements

The project can be extended in the future with:

* Interactive dashboards
* Multiple stock comparisons
* Additional technical indicators
* Candlestick charts
* Year-wise performance comparison
* Monthly and yearly return analysis
* Interactive Plotly visualizations
* More advanced financial analytics

---

## ⚠️ Disclaimer

This project is created for **educational and data analysis purposes only**.

The analysis is based on historical stock market data and should not be considered financial, investment, or trading advice.

Past performance does not guarantee future results.

---

## 👨‍💻 Author

**Chand Khimani**

### Course

**Data Analysis**

### Instructor

**Girish Gondaliya**

---

## ⭐ Project Highlights

```text
✔ Historical Stock Market Analysis
✔ Data Cleaning & Exploration
✔ Descriptive Statistics
✔ Closing Price Trend Analysis
✔ 20-Day Moving Average
✔ 50-Day Moving Average
✔ Trading Volume Analysis
✔ Daily Returns & Volatility
✔ Price-Volume Relationship
✔ Best & Worst Trading Days
✔ Correlation Heatmap
✔ Professional Data Visualizations
✔ Final Analytical Insights
```

---

### 📌 Project Status

**Completed — Ready for GitHub Submission 🚀**

---

## 📚 Conclusion

The **Stock Market Analysis** project demonstrates how Python and data analysis techniques can be used to transform historical stock market data into meaningful insights.

By combining data cleaning, statistical analysis, moving averages, trading volume, daily returns, correlation analysis, and visualizations, the project provides a structured view of historical stock market behavior.

This project demonstrates practical application of **Python, Pandas, NumPy, Matplotlib, and Seaborn** in a real-world Data Analysis scenario.

