# Students Performance Data Analysis Using Python

## Project Overview

This project focuses on analyzing student performance data using Python. The dataset contains students' demographic information, parental education, lunch type, test preparation status, and examination scores in Mathematics, Reading, and Writing.

The main objective is to clean categorical data and perform statistical analysis to understand students' academic performance.

## Objectives

* Load and explore the student performance dataset.

* Identify categorical and numerical features.

* Clean categorical values by removing extra spaces and standardizing capitalization.

* Calculate mean, median, and standard deviation for subject scores.

* Calculate quartiles (Q1, Q2, and Q3).

* Understand the distribution of students' examination scores.

## Dataset Information

**Dataset Name:** `StudentsPerformance.csv`

**Dataset Size:** 1,000 rows × 8 columns

### Features

| Column                      | Description                        |
| --------------------------- | ---------------------------------- |
| gender                      | Student gender                     |
| race/ethnicity              | Student's group classification     |
| parental level of education | Parent's educational qualification |
| lunch                       | Type of lunch plan                 |
| test preparation course     | Test preparation completion status |
| math score                  | Mathematics examination score      |
| reading score               | Reading examination score          |
| writing score               | Writing examination score          |

## Technologies Used

* Python

* Pandas

* NumPy

* Google Colab

## Data Preprocessing

### 1. Dataset Loading

Loaded the dataset using Pandas.

```
import pandas as pd
import numpy as np

df = pd.read_csv("StudentsPerformance.csv")
```

### 2. Dataset Inspection

Used the following functions to understand the dataset:

* `head()` – Displays the first five records.

* `columns` – Displays column names.

* `dtypes` – Identifies data types.

* `info()` – Provides dataset structure and non-null counts.

### 3. Feature Identification

**Categorical Features:**

* Gender

* Race/Ethnicity

* Parental Level of Education

* Lunch

* Test Preparation Course

**Numerical Features:**

* Math Score

* Reading Score

* Writing Score

### 4. Categorical Data Cleaning

Removed unnecessary leading and trailing spaces and standardized capitalization using `str.strip()` and `str.title()`.

```
for col in categorical_features:
    df[col] = df[col].str.strip().str.title()
```

This ensures consistent formatting of categorical values.

## Statistical Analysis

Calculated the following statistical measures for Mathematics, Reading, and Writing scores:

* **Mean:** Average examination score.

* **Median:** Middle value of the scores.

* **Standard Deviation:** Measures the spread of scores around the mean.

* **Q1 (25th Percentile):** Value below which 25% of scores fall.

* **Q2 (50th Percentile):** Median of the scores.

* **Q3 (75th Percentile):** Value below which 75% of scores fall.

### Statistical Results

| Statistical Measure | Math Score | Reading Score | Writing Score |
| ------------------- | ---------- | ------------- | ------------- |
| Mean                | 66.089     | 69.169        | 68.054        |
| Median              | 66.00      | 70.00         | 69.00         |
| Standard Deviation  | 15.163     | 14.600        | 15.196        |
| Q1 (25%)            | 57.00      | 59.00         | 57.75         |
| Q2 (50%)            | 66.00      | 70.00         | 69.00         |
| Q3 (75%)            | 77.00      | 79.00         | 79.00         |

## Key Findings

* The dataset contains 1,000 student records and 8 features.

* Five features are categorical, while three are numerical.

* Categorical values were standardized for consistent formatting.

* Reading has the highest mean score at 69.169.

* Mathematics has a mean score of 66.089.

* Writing has a mean score of 68.054.

* Reading has the lowest standard deviation among the three subjects, indicating slightly less variation in its scores.

* The median reading score is 70, compared with 66 in Mathematics and 69 in Writing.

## How to Run the Project

1. Download `StudentsPerformance.csv`.

2. Open Google Colab or Jupyter Notebook.

3. Import Pandas and NumPy.

4. Load the dataset using `pd.read_csv()`.

5. Inspect the dataset using `head()`, `columns`, `dtypes`, and `info()`.

6. Clean the categorical features.

7. Calculate statistical measures for all three subject scores.

8. Review the results.

## Conclusion

This project demonstrates how Python can be used for student performance data preprocessing and statistical analysis. By cleaning categorical features and calculating descriptive statistics, the project provides an understanding of students' academic performance and score distributions across Mathematics, Reading, and Writing.

