# Banking Project Overview

## Objective

- The goal of this project was to create an interactive Banking Dashboard that provides a comprehensive overview of client data, loans, deposits, and account balances. The dashboard is designed to support strategic decision-making by visualizing key banking metrics and understand how data is used to minimise the risk of losing money while lending to customers.

### 1. Data Collection & Import

- Sourced raw banking data including:

  - Client details

  - Loan information (bank loans, business lending)

  - Deposit types (savings, checking, foreign currency)

  - Account metrics and credit card usage

- Imported the data into MySQL to structure and normalize the data for further analysis.

### 2. Data Cleaning & Analysis

- Loaded the structured data into Jupyter Notebook using Python.

- Conducted:

  - Data cleaning (handling missing values, data type conversions)

  - Statistical analysis

  - Exploratory Data Analysis (EDA)

- Utilized libraries such as:

  - pandas for data manipulation

  - matplotlib and seaborn for visualization

```
categorical_cols = df[["BRId", "GenderId", "IAId", "Amount of Credit Cards", "Nationality", "Occupation", "Fee Structure", "Loyalty Classification", "Properties Owned", "Risk Weighting", "Income Band"]].columns
sns.set(style="whitegrid", palette="pastel")

for i, predictor in enumerate(df[categorical_cols].columns):
    plt.figure(figsize=(10, 5))
    ax = sns.countplot(data=df, x=predictor, hue=predictor, palette="Set2", order=df[predictor].value_counts().index)

  Rotate x-axis labels if too long
  plt.xticks(rotation=45, ha='right')
```


### 3. Dashboard Creation

- Imported the cleaned and processed data into Power BI.

- Designed an interactive dashboard that highlights:

  - Total Clients: 3,000

  - Total Loans: 4.38bn

  - Bank Loans: 1.77bn

  - Business Lending: 2.60bn

  - Total Deposits: 3.77bn (with breakdowns by account type)

  - Accounts: Checking (963.3M), Savings (698.7M), Foreign Currency (89.65M), Engagement Accounts

  - Total Credit Cards Issued: 3,000


### Tools & Technologies Used

- MySQL – Database structuring and querying

- Jupyter Notebook – Data preprocessing and statistical analysis

- Python Libraries – pandas, numpy, seaborn, matplotlib

- Power BI – Data visualization and dashboard creation


### Key Outcomes

- Enabled data-driven insights into customer and financial metrics

- Streamlined large data into visual, actionable information

- Supported business users in understanding banking KPIs across various dimensions (gender, relationship type, investment advisors, etc.)


## Conclusion

This project successfully demonstrates the end-to-end development of a data-driven Banking Dashboard, starting from raw data ingestion to the final visual analytics layer. By leveraging MySQL for data structuring, Python (Jupyter Notebook) for data preparation and analysis, and Power BI for dashboard creation, the project showcases a full-stack data workflow.

The dashboard provides clear, concise, and actionable insights into key financial and customer metrics, which can be used by stakeholders to monitor performance, optimize banking operations, and make informed strategic decisions. The process highlights the importance of data cleaning, exploration, and visualization in transforming complex datasets into valuable business intelligence.
