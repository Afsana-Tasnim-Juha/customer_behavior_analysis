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

# Customer Shopping Behavior Analysis

## Overview

This project analyzes customer shopping behavior using Python, SQL, and Power BI. The goal is to explore customer purchase patterns, clean and prepare the dataset, answer business questions using SQL, and present the results in an interactive Power BI dashboard.

This project demonstrates an end-to-end data analytics workflow, including data loading, exploratory data analysis, data cleaning, SQL-based analysis, and dashboard reporting.

## Dataset

The project uses a customer shopping behavior dataset.

**Dataset file:** `customer_shopping_behavior.csv.xlsx`

The dataset contains approximately **3,900 customer records** and includes information such as:

- Customer ID
- Age
- Gender
- Item Purchased
- Category
- Purchase Amount
- Location
- Size
- Color
- Season
- Review Rating
- Subscription Status
- Shipping Type
- Discount Applied
- Promo Code Used
- Previous Purchases
- Payment Method
- Frequency of Purchases

The dataset is used to understand customer spending behavior, product preferences, discount usage, subscription impact, and purchasing frequency.

## Project Files

```text
Customer-Behavior-Analysis/
│
├── customer_behavior_analysis.ipynb
├── customer_shopping_behavior.csv.xlsx
├── customer_behavior_sql_queries.sql
├── customer_behavior_dashboard.pbix
└── README.md
```

### File Description

- **`customer_behavior_analysis.ipynb`**: Jupyter Notebook used for loading the dataset, performing EDA, cleaning the data, creating new columns, and preparing the data for SQL analysis.
- **`customer_shopping_behavior.csv.xlsx`**: Source dataset containing customer shopping behavior records.
- **`customer_behavior_sql_queries.sql`**: SQL queries used to answer business questions from the cleaned dataset.
- **`customer_behavior_dashboard.pbix`**: Power BI dashboard file used to visualize key insights.

## Tools and Technologies

- **Python**: Data loading, exploratory data analysis, and data cleaning
- **Pandas**: Data manipulation and preprocessing
- **Jupyter Notebook**: Python analysis environment
- **SQLAlchemy**: Connecting Python with a SQL database
- **PostgreSQL / MySQL / SQL Server**: SQL-based data analysis
- **Power BI**: Dashboard creation and business reporting

## Project Steps

## 1. Data Loading

The dataset is loaded into Python using Pandas. Initial checks are performed to understand the data structure.

Key tasks include:

- Loading the customer shopping dataset
- Viewing the first few rows
- Checking data types
- Reviewing the number of rows and columns
- Identifying missing values
- Generating summary statistics

Example:

```python
import pandas as pd

df = pd.read_csv("customer_shopping_behavior.csv")
```

If using the Excel version of the dataset, update the code as follows:

```python
df = pd.read_excel("customer_shopping_behavior.csv.xlsx")
```

## 2. Exploratory Data Analysis

Exploratory Data Analysis is performed to understand customer behavior and identify patterns in the dataset.

EDA tasks include:

- Checking dataset shape and column information
- Reviewing missing values
- Exploring numerical and categorical columns
- Analyzing customer demographics
- Reviewing purchase amount patterns
- Understanding product categories, shipping types, and payment methods
- Comparing customer behavior across gender, age group, subscription status, and discount usage

## 3. Data Cleaning and Feature Engineering

The dataset is cleaned and prepared for analysis.

Main cleaning and transformation steps include:

- Handling missing values in `Review Rating`
- Filling missing review ratings using the median rating within each product category
- Standardizing column names by converting them to lowercase and replacing spaces with underscores
- Renaming `purchase_amount_(usd)` to `purchase_amount`
- Creating an `age_group` column
- Creating a `purchase_frequency_days` column from purchase frequency values
- Reviewing `discount_applied` and `promo_code_used`
- Dropping redundant columns when needed

These steps make the dataset easier to analyze in SQL and Power BI.

## 4. SQL Analysis

After cleaning, the dataset is loaded into a relational database such as PostgreSQL, MySQL, or SQL Server.

The SQL queries answer business questions such as:

- What is the total revenue generated by male vs. female customers?
- Which customers used a discount but still spent more than the average purchase amount?
- What are the top 5 products with the highest average review rating?
- How do purchase amounts compare between Standard and Express shipping?
- Do subscribed customers spend more than non-subscribed customers?
- Which products have the highest discount usage rate?
- How many customers are New, Returning, or Loyal?
- What are the top 3 most purchased products within each category?
- Are repeat buyers more likely to subscribe?
- What is the revenue contribution of each age group?

The SQL file included in this project is:

```text
customer_behavior_sql_queries.sql
```

## 5. Power BI Dashboard

A Power BI dashboard is created to present the results in a clear and interactive format.

The dashboard includes visuals such as:

- Revenue summary
- Customer segmentation
- Purchase trends
- Category and product-level insights
- Gender-based revenue comparison
- Subscription-based spending comparison
- Discount usage analysis
- Age group revenue contribution
- Product ranking and customer behavior insights

The dashboard file is:

```text
customer_behavior_dashboard.pbix
```

## Dashboard Results

The dashboard provides a business-friendly summary of customer shopping behavior.

Key insights include:

- Revenue differences across customer groups
- Top-performing product categories and items
- Customer purchase behavior by age group and gender
- Impact of subscription status on spending
- Discount usage patterns
- Repeat buyer and loyal customer segmentation
- Products with strong customer ratings and purchase activity

These insights can help businesses better understand customers, improve marketing strategies, evaluate discount effectiveness, and identify valuable customer segments.

## How to Run This Project

### 1. Clone or Download the Repository

```bash
git clone <repository-link>
cd Customer-Behavior-Analysis
```

### 2. Install Required Python Libraries

```bash
pip install pandas numpy sqlalchemy psycopg2-binary openpyxl
```

For MySQL or SQL Server, install the required database connector, such as:

```bash
pip install pymysql pyodbc
```

### 3. Open the Jupyter Notebook

```bash
jupyter notebook customer_behavior_analysis.ipynb
```

Run the notebook cells step by step to load, explore, clean, and prepare the dataset.

### 4. Load the Data into SQL

Create a database in PostgreSQL, MySQL, or SQL Server. Then update the database connection details in the notebook.

Use environment variables or placeholders instead of saving your real password directly in the notebook.

Example placeholder connection:

```python
from sqlalchemy import create_engine

username = "your_username"
password = "your_password"
host = "localhost"
port = "5432"
database = "customer_behavior"

engine = create_engine(
    f"postgresql+psycopg2://{username}:{password}@{host}:{port}/{database}"
)
```

Then load the cleaned DataFrame into the database:

```python
df.to_sql("customer", engine, if_exists="replace", index=False)
```

### 5. Run SQL Queries

Open `customer_behavior_sql_queries.sql` and run the queries in your preferred SQL environment.

The queries can be used in:

- pgAdmin for PostgreSQL
- MySQL Workbench for MySQL
- SQL Server Management Studio for SQL Server

Some SQL syntax may need small adjustments depending on the database system.

### 6. Open the Power BI Dashboard

Open the following file in Power BI Desktop:

```text
customer_behavior_dashboard.pbix
```

Refresh the data connection if needed, then explore the visuals and filters.

## Key Skills Demonstrated

- Data loading using Python
- Exploratory Data Analysis
- Data cleaning and preprocessing
- Feature engineering
- SQL querying and aggregation
- Relational database connection using SQLAlchemy
- Business question analysis using SQL
- Power BI dashboard development
- Data visualization and reporting
- End-to-end analytics workflow

## Conclusion

This project demonstrates a complete data analytics workflow from raw customer shopping data to actionable business insights. It shows practical experience in Python, SQL, and Power BI, making it suitable for demonstrating data analytics skills to recruiters and hiring managers.



## Conclusion

This project demonstrates a complete data analytics process from raw data to final dashboard reporting. It shows the ability to work with data using Python, SQL, and Power BI, while presenting insights in a clear and business-friendly way.

