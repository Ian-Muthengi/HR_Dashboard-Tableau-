# Human Resource Analysis

## Table of Contents

- [Project Overview](#project-overview)
- [Tools](#tools)
- [Data Analysis](#data-analysis)
- [Recommendations](#recommendations)

### Project Overview

This project delves into understanding the workforce and attrition rate within a company. Our aim is to detect patterns, offer recommendations based on evidence, and gain a comprehensive understanding of employees by analyzing different aspects of their job satisfaction and attrition rates. This includes examining factors such as educational attainment, the distribution of employees among different age brackets, employee turnover rates, levels of education, and levels of job satisfaction.

<img width="779" alt="hr dashboard picture" src="https://github.com/IanLiam/HR_Dashboard-Tableau-/assets/117744677/cef8b4dc-1646-43d9-aecd-beb966b5e4da">



### Data Sources
The dataset utilized for this analysis is the 'HR_data.csv' file, which comprises comprehensive details on employees.

### Tools
- Excel - Data Cleaning  [Download here](https://www.microsoft.com/en-us/microsoft-365/download-office)
- Python - Data Cleaning  [Download here](https://www.anaconda.com/download)
- SQL Server - Data Analysis [Download here](https://www.microsoft.com/en-us/sql-server/sql-server-downloads)
- Tableau - Creating reports  [Download here](https://www.tableau.com/community/public)
  
### Data cleaning/ Preparation
In the initial data preparation phase, we performed the following tasks:

1. Data loading and inspection.
2. Handling missing values.
3. Data cleaning and formatting.

### Exploratory Data Analysis
EDA involved exploring the Human Resource data to answer key questions, such as:

- What is the highest number of employees by age group?
- Which attrition rate dominates in terms of the number of employees based on their level of education?"
- Which department has the highest attrition rate?
  
### Data Analysis
Features worked with:

1. SQL
```sql
-- Selecting with a condition
SELECT * FROM HR_data
where department = 'Life Sciences';
```

2. Python
```python
# Transposing data
import pandas as pd

# Replace 'input.csv' with the path to your CSV file
input_file = r'C:\Users\ian.muthengi\Downloads\HR_data.xlsx'

# Read the CSV file into a pandas DataFrame
df = pd.read_excel(input_file)

# Transpose the DataFrame
df_transposed = df.transpose()

# Replace 'output_transposed.csv' with the desired output file name
output_file = 'C:/Users/ian.muthengi/Downloads/transposed_HR_data.xlsx'

# Write the transposed DataFrame to a new CSV file
df_transposed.to_excel(output_file, index=True, header=False)
```
### Results/Findings
The analysis results are summarized as follows:

1. The age group of 31-33 has the highest number of employees attriting the company.
2. The R&D department has the largest count of employees leaving the organization.
3. The level of education in Life Sciences dominates the employee attrition rates.

### Recommendations
Based on the analysis, we recommend the following actions:

1. Conducting exit interviews or surveys with employees 
2. Assess the workload and stress levels.
3. Recognize and reward the contributions of employees to boost morale and job satisfaction.
4. Foster open communication channels within the employees and encourage feedback from employees.

### Limitations
- Attrition data might not always be accurately recorded or updated in HR systems, leading to discrepancies in the actual attrition rates.
- Some employees may leave without formal notification or without the HR department's knowledge, resulting in missing data points and incomplete records.
