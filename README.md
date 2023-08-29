## Introduction

![](istock.jpg)

image from istock.com

The Employees Data Analysis Report provides a comprehensive overview of key insights gathered from the analysis of employee data within the Company. The analysis encompasses various aspects of employee information, aiming to uncover trends, patterns, and actionable insights that can contribute to informed decision-making and improved organizational performance.

## Dataset Overview
The dataset consisted of several vital columns including,
- Employee ID
- Full Name
- Job Title
- Department
- Business Unit
- Gender
- Ethnicity
- Age
- Hire Date
- Annual Salary
- Bonus Percentage
- Country
- City
- Exit Date

## Project Objectives:

•	Analyze employee data using SQL to uncover insights.
•	Transform the insights into meaningful KPIs.
•	Create an interactive Power BI dashboard to visualize the KPIs.

## Methodology

I opened the CSV dataset and renamed some columns; employee ID to employee_ID, Full name to Full_name, Job title to Job_title, Business unit to Business_unit, Hire Date to Hire_date, Annual salary to Annual_salary, Bonus % to Bonus_percentage and Exit date to Exit_date. Then I saved the file as Excel 97 - 2003 template. 

Afterward, I imported the employee sample data into the Project database using Microsoft SQL Server Management Studio. By crafting a set of thoughtfully designed SQL queries, I accomplished the project objectives. These queries were strategically formulated to address various aspects of the dataset, enabling the extraction of specific insights. Each query was accompanied by detailed comments explaining the rationale behind its construction. Through the skillful application of appropriate aggregate functions, precise grouping techniques, and systematic data ordering, I effectively aggregated and summarized the dataset. This process yielded meaningful and actionable results, contributing to the overall project's success.

## SQL Queries and Analysis

### Sample Analysis Questions:

--1. How many employees are there in each department?

SELECT department, COUNT(DISTINCT employee_id) AS num_of_employees
FROM employees
GROUP BY department
ORDER BY num_of_employees;

![](1.jpg)

This query groups the employees by their department and calculates the count of employees in each department using the COUNT aggregate function. The result shows the department and the corresponding number of employees in that department.


--2. What is the average age of employees in the Sales department?

SELECT department, ROUND(AVG(age), 2) AS avg_age
FROM employees
WHERE department = 'Sales'
GROUP BY department;

![](2.jpg)

This query calculates the average age of employees in the Sales department directly from the "age" column.

--3. Who are the top 5 highest-paid employees in the company?

SELECT TOP 5 full_name, annual_salary
FROM employees
ORDER BY annual_salary DESC;

![](3.jpg)




