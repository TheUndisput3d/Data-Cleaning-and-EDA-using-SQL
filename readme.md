# Laptop Dataset Cleaning and Exploratory Data Analysis (EDA) Using SQL

This project demonstrates a complete workflow for data cleaning and exploratory data analysis (EDA) using pure SQL on a structured laptop specification dataset. It covers raw data preprocessing, feature engineering, statistical summarization, and categorical analysis, all implemented with SQL queries.

**This repository also showcases my SQL analysis skills through practical, end-to-end transformations and insights derived directly using SQL.**

## Overview

The repository contains two SQL scripts:

1. `data-cleaning-sql.sql` - A comprehensive data cleaning pipeline.
2. `eda_laptop_dataset.sql` - SQL-based exploratory data analysis on the cleaned dataset.

These scripts are intended for those who want to learn or demonstrate how SQL can be used to clean and analyze tabular data without relying on external programming languages or tools.

## Files Included

| File                      | Description                                                                 |
|---------------------------|-----------------------------------------------------------------------------|
| `data-cleaning-sql.sql`   | Cleans raw laptop data, removes unnecessary columns, handles null values, converts data types, extracts CPU/GPU brands and names, splits memory types, and performs general feature engineering. |
| `eda_laptop_dataset.sql`  | Analyzes the cleaned dataset by calculating summary statistics, detecting outliers, performing bucketed price distribution, generating categorical group summaries, and conducting basic feature engineering like screen size and pixel density (PPI). |

## Key Techniques Used

### Data Cleaning (`data-cleaning-sql.sql`)
- Dropping irrelevant or null-heavy rows
- Data type conversions (e.g., Ram from string to integer)
- Unit removal and normalization (e.g., GB, kg, GHz)
- Feature extraction from complex strings (e.g., CPU, GPU)
- Memory breakdown into `primary_storage` and `secondary_storage`
- Screen resolution parsing and touchscreen detection
- Operating system categorization

### EDA (`eda_laptop_dataset.sql`)
- Head, tail, and random sampling
- Summary statistics (count, min, max, average, standard deviation, percentiles)
- Outlier detection using IQR method
- Price bucket grouping
- Categorical breakdown by company, CPU brand, and touchscreen availability
- Screen size classification and one-hot encoding examples

## Use Cases

- Data pre-processing before ML or visualization
- Feature engineering using SQL
- Practicing SQL on real-world data
- Learning SQL-based EDA without Python or R

## Requirements

- MySQL 8.0+ or compatible SQL database supporting:
  - `PERCENTILE_CONT()`
  - `REGEXP_SUBSTR()`
  - `SUBSTRING_INDEX()`

