# Global Layoffs Data Analysis using SQL

## Project Overview

This project demonstrates an end-to-end data analysis workflow using SQL on a global layoffs dataset. The project involves cleaning raw data, standardizing inconsistent values, handling missing information, and performing exploratory data analysis (EDA) to identify trends and patterns in layoffs across companies, industries, and time.

The goal is to transform a raw dataset into a structured and reliable dataset that can be used for meaningful analysis and business insights.

## Dataset Description

The dataset contains information about layoffs across companies worldwide. The key attributes include:

* Company
* Location
* Industry
* Total Laid Off
* Percentage Laid Off
* Date
* Company Stage
* Country
* Funds Raised (Millions)

## Project Structure

Data Cleaning Script


Exploratory Data Analysis Script


## Data Cleaning Process

### 1. Creating a Staging Table

A staging table was created to store a copy of the raw dataset. This ensures that the original dataset remains unchanged during cleaning.

### 2. Removing Duplicate Records

Duplicate rows were identified using the `ROW_NUMBER()` window function and removed to ensure data accuracy.

### 3. Standardizing Data

Several inconsistencies were corrected:

* Removed extra spaces from company names
* Standardized industry names (e.g., variations of "crypto" converted to "Crypto")
* Cleaned country names by removing punctuation
* Converted the date column from text format to SQL DATE format

### 4. Handling Missing Values

Missing and blank values were handled by:

* Converting empty values into NULL
* Filling missing industry values using other records of the same company
* Removing rows with insufficient information

### 5. Final Dataset Preparation

Helper columns used during cleaning (such as duplicate row identifiers) were removed to produce a final clean dataset ready for analysis.

## Exploratory Data Analysis (EDA)

After cleaning the data, several analytical queries were performed to understand layoffs trends.

Key analysis performed:

* Identified companies with the highest layoffs
* Analyzed layoffs by industry
* Examined layoffs trends by year
* Identified companies with 100% layoffs
* Analyzed monthly layoffs trends
* Compared layoffs with funding raised by companies

## Skills Demonstrated

* SQL Data Cleaning
* Window Functions (ROW_NUMBER)
* Data Transformation
* Handling Missing Values
* Exploratory Data Analysis (EDA)
* Aggregation and Grouping
* Time-based Analysis

## Tools Used

* SQL
* MySQL

## Outcome

The project demonstrates how raw data can be transformed into a clean dataset and analyzed to uncover meaningful insights about layoffs trends across companies, industries, and time periods.

This project reflects real-world data analyst tasks including data cleaning, data preparation, and exploratory analysis.
