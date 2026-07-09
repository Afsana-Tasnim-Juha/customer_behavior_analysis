# customer_behavior_analysis
Data analytics project showcasing customer behavior analysis using python, sql and power Bi.

# Data Analytics Project

## Overview

This project demonstrates an end-to-end data analytics workflow using Python, SQL, and Power BI. The goal of the project is to load and analyze a dataset, clean and prepare the data, run SQL queries for deeper insights, and build an interactive Power BI dashboard to present key findings.

The project highlights practical skills in data cleaning, exploratory data analysis, database querying, and business intelligence reporting.

## Dataset

The dataset used in this project contains structured data related to business operations, sales, customers, products, or other analytical use cases.

The dataset includes fields such as:

* Date or time-based information
* Customer or category details
* Numerical performance metrics
* Transaction or record-level data
* Other relevant business attributes

The data was loaded into Python for analysis and later used in SQL and Power BI for reporting.

## Tools and Technologies

The following tools were used in this project:

* **Python**: Data loading, cleaning, and exploratory data analysis
* **Pandas**: Data manipulation and preprocessing
* **Matplotlib / Seaborn**: Data visualization during EDA
* **SQL**: Querying and analyzing structured data
* **PostgreSQL / MySQL / SQL Server**: Relational database management
* **Power BI**: Dashboard development and data visualization
* **Jupyter Notebook**: Python analysis environment

## Project Steps

### 1. Data Loading

The dataset was loaded into Python using Pandas. Initial checks were performed to understand the structure of the data, including:

* Number of rows and columns
* Column names and data types
* Missing values
* Duplicate records
* Basic summary statistics

### 2. Exploratory Data Analysis

Exploratory Data Analysis was performed to understand patterns, trends, and relationships in the data.

Key EDA tasks included:

* Analyzing numerical and categorical variables
* Identifying missing or inconsistent values
* Detecting outliers
* Reviewing distributions of key metrics
* Finding trends over time
* Exploring relationships between important variables

### 3. Data Cleaning

The dataset was cleaned and prepared for analysis. The cleaning process included:

* Handling missing values
* Removing duplicate records
* Correcting incorrect data types
* Standardizing column names
* Fixing inconsistent category values
* Creating new calculated fields when needed
* Preparing the final clean dataset for SQL and Power BI

### 4. SQL Analysis

After cleaning, the data was loaded into a relational database such as PostgreSQL, MySQL, or SQL Server.

SQL queries were written to answer important business questions, such as:

* Total records and overall summary metrics
* Sales or performance trends by time period
* Top-performing categories, products, or regions
* Customer or user-level insights
* Aggregated KPIs for dashboard reporting

The SQL analysis helped validate the data and generate insights for the dashboard.

### 5. Power BI Dashboard

A Power BI dashboard was created to present the key findings in a clear and interactive format.

The dashboard includes:

* KPI cards
* Trend charts
* Category or segment breakdowns
* Filters and slicers
* Summary tables
* Interactive visuals for business insights

The dashboard allows users to explore the data and understand performance from different perspectives.

## Dashboard Results

The Power BI dashboard provides a clear overview of the most important insights from the dataset.

Key results include:

* Identification of major trends and patterns
* Summary of important business metrics
* Comparison across categories, regions, or time periods
* Detection of high-performing and low-performing segments
* Improved understanding of the data through interactive visuals

These results can support better decision-making and business analysis.

## How to Run This Project

### 1. Clone the Repository

```bash
git clone <repository-link>
cd <repository-folder>
```

### 2. Install Required Python Libraries

```bash
pip install pandas numpy matplotlib seaborn sqlalchemy
```

### 3. Open the Jupyter Notebook

```bash
jupyter notebook
```

Then open the notebook file and run the cells step by step.

### 4. Load the Dataset

Place the dataset file in the project folder and update the file path in the Python notebook if needed.

Example:

```python
import pandas as pd

df = pd.read_csv("dataset.csv")
```

### 5. Run the SQL Queries

Import the cleaned dataset into PostgreSQL, MySQL, or SQL Server. Then run the SQL scripts provided in the project folder.

Example SQL query:

```sql
SELECT 
    category,
    COUNT(*) AS total_records,
    SUM(sales) AS total_sales
FROM table_name
GROUP BY category
ORDER BY total_sales DESC;
```

### 6. Open the Power BI Dashboard

Open the `.pbix` file in Power BI Desktop. Refresh the data connection if needed and explore the dashboard visuals.

## Project Structure

```text
Data-Analytics-Project/
│
├── data/
│   └── dataset.csv
│
├── notebooks/
│   └── eda_and_cleaning.ipynb
│
├── sql/
│   └── analysis_queries.sql
│
├── dashboard/
│   └── powerbi_dashboard.pbix
│
├── output/
│   └── cleaned_dataset.csv
│
└── README.md
```

## Key Skills Demonstrated

* Data loading and preprocessing using Python
* Exploratory Data Analysis
* Data cleaning and transformation
* SQL querying and aggregation
* Database connection and analysis
* Power BI dashboard development
* Business insight generation
* End-to-end analytics workflow

## Conclusion

This project demonstrates a complete data analytics process from raw data to final dashboard reporting. It shows the ability to work with data using Python, SQL, and Power BI, while presenting insights in a clear and business-friendly way.

