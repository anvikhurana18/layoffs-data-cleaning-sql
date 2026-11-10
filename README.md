# Data Cleaning Using SQL – Company Layoffs Dataset

## Project Overview

This project focuses on cleaning and transforming a real-world company layoffs dataset using SQL in MySQL Workbench.

The dataset contains information about employee layoffs across different companies, industries, and countries. It includes details such as the number of employees laid off, percentage of workforce affected, company funding, company stage, and layoff dates.

The main objective of this project is to identify and resolve data quality issues, remove duplicate records, standardize inconsistent data, handle missing values, and prepare a clean dataset for further analysis.

## Project Objectives

- Identify and remove duplicate records.
- Standardize inconsistent company and industry names.
- Clean country names and date formats.
- Identify and handle NULL and blank values.
- Populate missing industry information using SQL JOINs.
- Remove records with missing layoff information.
- Prepare a clean dataset for further analysis.

## Dataset Description

The dataset contains the following columns:

| Column | Description |
|---|---|
| Company | Name of the company |
| Location | Company location |
| Industry | Industry in which the company operates |
| Total Laid Off | Number of employees laid off |
| Percentage Laid Off | Percentage of employees affected |
| Date | Date of layoff announcement |
| Stage | Company's funding or growth stage |
| Country | Country where the company operates |
| Funds Raised (Millions) | Total funds raised by the company in millions |

## Tools & Technologies

- **Database:** MySQL
- **SQL Editor:** MySQL Workbench
- **Language:** SQL
- **Version Control:** GitHub

## Data Cleaning Process

### 1. Creating Staging Tables
- Created staging tables using `CREATE TABLE LIKE`.
- Copied the original dataset into staging tables.
- Preserved the original data while performing cleaning operations.

### 2. Removing Duplicate Records
- Used `ROW_NUMBER()` window function to identify duplicate records.
- Applied `PARTITION BY` across multiple columns.
- Used Common Table Expressions (CTEs) to identify duplicate entries.
- Removed duplicate records using the `DELETE` statement.

### 3. Standardizing Data
- Used `TRIM()` to remove unnecessary spaces from company names.
- Standardized different variations of Crypto industry names into a single category.
- Removed trailing periods from United States country values.

### 4. Handling Date Formats
- Used `STR_TO_DATE()` to convert text-based dates into proper date values.
- Modified the date column to the DATE data type using `ALTER TABLE`.

### 5. Handling NULL and Blank Values
- Identified missing and blank industry values.
- Converted blank industry entries into NULL values.
- Used self-joins to populate missing industry information using matching company names and locations.
- Identified records where both total layoffs and percentage laid off were missing.
- Removed records with both layoff values missing.

### 6. Final Data Preparation
- Removed the temporary `row_num` column.
- Retrieved the final cleaned dataset using SELECT statements.
- Prepared the cleaned data for further analysis.

## SQL Concepts Used

This project demonstrates practical implementation of:

- SELECT and WHERE statements
- CREATE TABLE and INSERT INTO
- ROW_NUMBER() Window Function
- Common Table Expressions (CTEs)
- DELETE and UPDATE statements
- TRIM() and STR_TO_DATE()
- LIKE operator
- IS NULL and IS NOT NULL
- INNER JOIN / Self Join
- ALTER TABLE
- GROUP BY and PARTITION BY

## Project Files

| File Name | Description |
|---|---|
| `layoffs.csv` | Original raw dataset |
| `layoffs_data_cleaning.sql` | SQL queries used for data cleaning |
| `cleaned_layoffs.csv` | Final cleaned dataset |
| `README.md` | Project documentation |

## Future Scope

The cleaned dataset can be used for further Exploratory Data Analysis (EDA) to explore:

- Which industries experienced the highest number of layoffs?
- Which companies laid off the most employees?
- Which countries were most affected by layoffs?
- How did layoffs change over time?
- Which company funding stages experienced significant layoffs?
- Is there a relationship between company funding and employee layoffs?

## Key Learnings

Through this project, I gained hands-on experience in:

- Working with real-world datasets.
- Identifying and resolving data quality issues.
- Writing SQL queries for data cleaning.
- Using window functions and CTEs.
- Handling missing and duplicate records.
- Standardizing inconsistent data.
- Using joins to retrieve and update missing information.
- Preparing structured datasets for further analysis.

## Author

**Anvi**

Aspiring Data Analyst

Skills: SQL | MySQL | Data Cleaning | Data Analysis

GitHub: https://github.com/anvikhurana18

---

*This project is part of my learning journey in Data Analytics, focusing on developing practical SQL skills through real-world datasets.*
