# Banking Project Overview

## Objective

- The goal of this project was to create an interactive Banking Dashboard that provides a comprehensive overview of client data, loans, deposits, and account balances. The dashboard is designed to support strategic decision-making by visualizing key banking metrics.

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

- **MySQL – Database structuring and querying**

- Jupyter Notebook – Data preprocessing and statistical analysis

- Python Libraries – pandas, numpy, seaborn, matplotlib

- Power BI – Data visualization and dashboard creation
