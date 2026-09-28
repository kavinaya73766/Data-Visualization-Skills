# Healthcare Dataset Analysis Using Python

## Project Overview

This project focuses on analyzing a healthcare dataset containing patient information, medical conditions, admission details, billing amounts, and discharge dates.

The main objective is to clean, preprocess, and explore healthcare data using Python libraries such as Pandas, Matplotlib, and Seaborn.

## Objectives

* Load and understand the healthcare dataset.
* Identify missing values and data types.
* Convert date columns into datetime format.
* Analyze patient admission types.
* Calculate hospital stay duration.
* Perform descriptive statistical analysis.
* Understand billing amount distribution.

## Dataset Information

**Dataset Name:** `healthcare_dataset.csv`

**Dataset Size:** 500 rows × 9 columns

### Features

| Column            | Description                   |
| ----------------- | ----------------------------- |
| Patient_ID        | Unique patient identifier     |
| Gender            | Patient gender                |
| Age               | Patient age                   |
| Medical_Condition | Patient's medical condition   |
| Admission_Date    | Date of hospital admission    |
| Admission_Type    | Routine, Emergency, or Urgent |
| Medical_Code      | Medical diagnosis code        |
| Billing_Amount    | Hospital billing amount       |
| Discharge_Date    | Date of hospital discharge    |

## Technologies Used

* Python
* Pandas
* Matplotlib
* Seaborn
* Google Colab

## Data Preprocessing

### 1. Dataset Loading

Loaded the healthcare dataset using Pandas.

### 2. Dataset Inspection

Used the following functions to understand the dataset:

* `head()` – Displays the first five records.
* `columns` – Displays column names.
* `shape` – Shows the number of rows and columns.
* `dtypes` – Displays data types.
* `describe()` – Provides descriptive statistics.

### 3. Missing Value Detection

Identified 15 missing values in the `Medical_Code` column.

All other columns contain zero missing values.

### 4. Date Conversion

Converted `Admission_Date` and `Discharge_Date` into datetime format for date-based calculations.

### 5. Admission Type Standardization

Converted admission type values into lowercase to maintain consistent formatting.

### 6. Hospital Stay Calculation

Created a new column called `Hospital_Stay_Days` by calculating the difference between discharge date and admission date.

## Exploratory Data Analysis

### Admission Type Distribution

| Admission Type | Patient Count |
| -------------- | ------------: |
| Routine        |           196 |
| Emergency      |           188 |
| Urgent         |           116 |

### Billing Amount Statistics

| Statistical Measure |     Value |
| ------------------- | --------: |
| Count               |       500 |
| Mean                | 7,249.001 |
| Median              |     6,950 |
| Standard Deviation  |  3,198.97 |
| Minimum             |     2,300 |
| Maximum             |    14,200 |

### Age Statistics

* Average patient age: 50.11 years
* Minimum age: 22 years
* Maximum age: 78 years

## Python Libraries

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```

## How to Run the Project

1. Download or upload `healthcare_dataset.csv` to Google Colab.
2. Import the required Python libraries.
3. Load the dataset using Pandas.
4. Perform data inspection and preprocessing.
5. Calculate hospital stay duration.
6. Perform statistical analysis and explore the dataset.

## Key Findings

* The dataset contains 500 patient records and 9 columns.
* The `Medical_Code` column contains 15 missing values.
* Routine admissions account for 196 records.
* The average billing amount is approximately 7,249.
* The average patient age is approximately 50 years.
* Hospital stay duration was calculated using admission and discharge dates.

## Conclusion

This project demonstrates how Python can be used to inspect, clean, preprocess, and analyze healthcare data. The analysis provides an understanding of patient demographics, admission patterns, billing amounts, and hospital stay duration.


