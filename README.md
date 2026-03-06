# SQL Data Cleaning Project – Layoffs Dataset

## Overview

This project demonstrates a complete data cleaning workflow using SQL. The dataset contains information about company layoffs, including company name, location, industry, total layoffs, percentage laid off, funding, and date. The goal is to clean and prepare the raw dataset so that it can be used for accurate data analysis.

## Dataset

The dataset includes the following fields:

* Company
* Location
* Industry
* Total Laid Off
* Percentage Laid Off
* Date
* Stage
* Country
* Funds Raised (Millions)

## Data Cleaning Steps

### 1. Creating a Staging Table

A staging table (`layoffs_staging`) is created to store a copy of the original dataset. This ensures that the raw dataset remains unchanged while cleaning operations are performed.

### 2. Removing Duplicate Records

Duplicate rows are identified using the `ROW_NUMBER()` window function and removed from the dataset to maintain data accuracy.

### 3. Standardizing Data

Inconsistent values are standardized to maintain uniformity:

* Trimmed unnecessary spaces from company names.
* Standardized industry values (e.g., variations of "crypto" converted to "Crypto").
* Cleaned country names by removing unnecessary characters.
* Converted the date column into proper DATE format.

### 4. Handling Missing or Null Values

Missing values were identified and handled appropriately:

* Blank industry values were converted to NULL.
* Missing industry values were populated using data from similar records within the same company.
* Rows with insufficient information were removed.

### 5. Final Dataset Preparation

After cleaning the data, unnecessary columns such as the duplicate identifier (`row_num`) were removed to create a clean dataset ready for analysis.

## Skills Demonstrated

* SQL Data Cleaning
* Window Functions (ROW_NUMBER)
* Data Standardization
* Handling Missing Values
* Data Transformation
* Table Manipulation

## Tools Used

* MySQL
* SQL

## Outcome

The final cleaned dataset is consistent, accurate, and ready for exploratory data analysis and visualization in tools such as Power BI, Tableau, or Python.
