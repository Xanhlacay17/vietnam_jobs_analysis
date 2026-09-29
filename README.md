# Vietnam Jobs Market: Data Cleaning & Preprocessing Pipeline

[![Open In Colab](https://google.com)](https://colab.research.google.com/drive/159dNJXn8V1MUI__cxjdbuoJ_ir5FDIpP#scrollTo=aFQ-S3Fk1Jaf)

## 📌 Project Overview
This project builds an automated data cleaning and preprocessing pipeline using **Python** and **pandas** to process a raw web-scraped dataset of job advertisements in Vietnam. The primary objective is to transform inconsistent, noisy text and tabular data into a structured, analysis-ready format for downstream Labor Market Analytics or Salary Prediction modeling.

## 📊 Dataset Description
- **Source:** [Kaggle - Vietnam Jobs Dataset (by Nguyen Chi Tinh)](https://kaggle.com)
- **Data Scope:** Features job postings across major Vietnamese cities (e.g., Ho Chi Minh City, Hanoi) and multiple occupational domains.
- **Problem Statement:** The raw dataset contained high structural noise, mixed languages (Vietnamese/English), inconsistent data types, and unstandardized text fields (e.g., salary ranges, locations, and posting dates).

## 🛠️ Data Cleaning Steps & Engineering Workflows

### 1. Handling Missing Data & Duplicates
- **Deduplication:** Identified and eliminated duplicate job advertisements based on unique job titles and company profiles.
- **Missing Value Imputation:** Dropped rows with missing critical features (e.g., job titles). Handled missing numerical fields using median values to preserve distribution profiles.

### 2. Feature Standardization & Extraction
- **Salary Standardization:** Parsed complex, non-numeric salary text strings (e.g., "10 - 15 triệu", "Thỏa thuận") into clean numerical metrics, establishing explicit `Min_Salary` and `Max_Salary` attributes in VND.
- **Geographic Normalization:** Consolidated mixed and misspelled location strings into standardized regional categories (e.g., mapping "TP. HCM", "Hồ Chí Minh", and "HCMC" uniformly to "Ho Chi Minh City").
- **Temporal Parsing:** Converted text-based posting dates into uniform `datetime` objects to unlock time-series analytics (Extracting Year, Month, and Weekday features).

### 3. Text Normalization
- Stripped redundant whitespaces, removed special HTML characters from web-scraping, and unified character encodings to ensure text consistency across titles and job requirements.

## 🚀 Technologies Used
- **Language:** Python 3
- **Core Library:** pandas (Data Manipulation), NumPy (Mathematical & Array Operations)
- **Environment:** Google Colab

## 📈 Key Pipeline Results
- Reclaimed **100% data type integrity** across all schema attributes.
- Effectively converted un Rain-text features into structured metrics ideal for Exploratory Data Analysis (EDA).
