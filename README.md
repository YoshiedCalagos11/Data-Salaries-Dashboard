# Data Science Salaries Dataset

This repository contains a dataset of data science salaries, which includes information about various job titles, salaries, and other related details. The dataset is stored in the `ds_salaries.csv` file.

## Dataset Overview

The dataset includes the following columns:

- **id**: Unique identifier for each record.
- **work_year**: The year the salary was recorded.
- **experience_level**: The experience level of the employee (e.g., Junior, Mid, Senior).
- **employment_type**: The type of employment (e.g., Full-time, Part-time).
- **job_title**: The job title of the employee.
- **salary**: The salary amount in the original currency.
- **salary_currency**: The currency of the salary.
- **salary_in_usd**: The salary amount converted to USD.
- **employee_residence**: The country of residence of the employee.
- **remote_ratio**: The ratio of remote work (0, 50, 100).
- **company_location**: The country where the company is located.
- **company_size**: The size of the company (e.g., Small, Medium, Large).

## Key Metrics

- **Average Salary**: The average salary for each job title.
- **Top Salaries**: The top 5 highest salaries in the dataset.
- **Employee Count**: The number of employees by experience level.
- **Total Salary by Location**: The total salary paid by companies in different locations.

## How to Use the Dataset

1. **Download the CSV File**: Download the `ds_salaries.csv` file from this repository.
2. **Load the Data**: Use your preferred data analysis tool (e.g., Python, R, Excel) to load the dataset.
3. **Analyze the Data**: Perform various analyses to gain insights into data science salaries, such as calculating average salaries, identifying top-paying job titles, and analyzing salary distributions by location and experience level.

   For example, to identify the top 5 highest salaries, you can use the following SQL query:
   ```sql
   SELECT job_title AS 'Job Title', 
          CONCAT('$', FORMAT(salary_in_usd, 2)) AS 'Salary'
   FROM ds_salaries
   ORDER BY salary_in_usd DESC
   LIMIT 5;

Resources
Data Science Job Salaries on Kaggle
https://www.kaggle.com/datasets/ruchi798/data-science-job-salaries
