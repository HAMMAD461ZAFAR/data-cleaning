# data-cleaning
# Project 1: Data Collection & Cleaning

A beginner-friendly data cleaning project built with Python and Pandas. This project takes a messy, real-world-style sales dataset and walks through the full process of identifying and fixing common data quality issues.

## 📌 Overview

Raw data is rarely clean. This project simulates that reality using a sales orders dataset containing:
- Duplicate records
- Missing values
- Inconsistent text formatting (casing, whitespace)
- Mixed date formats
- Invalid/negative numeric values
- Outliers

The goal is to transform this messy dataset into a clean, analysis-ready CSV file using Pandas.

## 🛠️ Tools Used
- Python 3
- Pandas

## 📂 Files
- `uncleaned_sales_data.csv` — the raw, messy dataset
- `clean_data.py` — the script that performs the cleaning
- `cleaned_sales_data.csv` — the final cleaned output

## 🔍 Data Issues Identified
- Duplicate rows (same customer/product/date)
- Missing values across multiple columns
- Inconsistent casing (`electronics` vs `Electronics`)
- Extra whitespace in text fields
- Mixed date formats (`2024-01-15`, `01/16/2024`, `15-Jan-2024`)
- Invalid dates (e.g. `2024-13-45`)
- Negative prices
- Unrealistic outlier values (e.g. quantity of 999)

## ✅ Cleaning Steps
1. Stripped whitespace and standardized text casing
2. Converted placeholder text (`N/A`, `not available`) into proper missing values
3. Removed duplicate rows
4. Standardized all dates into a consistent datetime format
5. Converted numeric columns to proper number types
6. Fixed negative prices and flagged outlier quantities
7. Filled missing values (median for numbers, placeholders for text)
8. Added a derived `total_amount` column
9. Verified the cleaned data with assertions
10. Exported the final cleaned dataset

## 🚀 How to Run
```bash
pip install pandas
python clean_data.py
```

## 📈 Result
- Rows before cleaning: 20
- Rows after cleaning: 18 (2 duplicates removed)
- All missing values handled
- All dates standardized to a single format
- No negative prices remain

## 🎯 What I Learned
This project helped me practice core data cleaning skills using Pandas: handling missing data, removing duplicates, standardizing formats, and validating results — all essential steps before any real data analysis or machine learning work.
