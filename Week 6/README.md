# Healthcare Data Analysis Using Python

## Project Overview

This project focuses on analyzing a healthcare dataset containing patient details, medical conditions, hospital admissions, insurance providers, billing amounts, medications, and test results.

The main objective is to perform data cleaning, preprocessing, exploratory data analysis (EDA), statistical analysis, and data visualization using Python.

## Objectives

* Understand and explore healthcare data.

* Identify missing values and data types.

* Convert date columns into datetime format.

* Calculate hospital stay duration.

* Analyze billing amounts across medical conditions and insurance providers.

* Visualize billing distributions using advanced charts.

* Study monthly patient admission trends.

* Identify relationships between age, hospital stay duration, and billing amount.

## Dataset Information

**Dataset Name:** `healthcare_dataset.csv`

**Dataset Size:** 55,500 rows × 15 columns

### Features

| Column             | Description                    |
| ------------------ | ------------------------------ |
| Name               | Patient name                   |
| Age                | Patient age                    |
| Gender             | Patient gender                 |
| Blood Type         | Patient blood group            |
| Medical Condition  | Patient's medical condition    |
| Date of Admission  | Hospital admission date        |
| Doctor             | Assigned doctor                |
| Hospital           | Hospital name                  |
| Insurance Provider | Patient's insurance company    |
| Billing Amount     | Total hospital billing amount  |
| Room Number        | Assigned room number           |
| Admission Type     | Urgent, Emergency, or Elective |
| Discharge Date     | Hospital discharge date        |
| Medication         | Prescribed medication          |
| Test Results       | Medical test results           |

## Technologies Used

* Python

* Pandas

* Matplotlib

* Seaborn

* Google Colab

## Data Preprocessing

### 1. Dataset Loading

Loaded the healthcare dataset using Pandas.

### 2. Data Inspection

Used the following functions to understand the dataset:

* `head()` – Displays the first five records.

* `columns` – Displays column names.

* `dtypes` – Identifies data types.

* `shape` – Shows the number of rows and columns.

* `isnull().sum()` – Checks missing values.

### 3. Missing Value Detection

Checked all columns for missing values.

**Result:** No missing values were found in the dataset.

### 4. Date Conversion

Converted `Date of Admission` and `Discharge Date` into datetime format for date-based analysis.

### 5. Hospital Stay Duration

Created a new column called `stay Duration` by calculating the difference between discharge date and admission date.

```
df["stay Duration"] = (
    df["Discharge Date"] - df["Date of Admission"]
).dt.days
```

### 6. Monthly Admission Extraction

Extracted the month from the admission date to analyze monthly patient admissions.

## Exploratory Data Analysis (EDA)

### 1. Billing Analysis by Medical Condition and Insurance Provider

Grouped the dataset by medical condition and insurance provider to calculate total and average billing amounts.

### 2. Stacked Bar Chart

Visualized average billing amounts across medical conditions and insurance providers using a stacked bar chart.

**Purpose:** To compare average hospital billing amounts across different medical conditions and insurance providers.

### 3. Violin Plot – Billing by Medical Condition

Used a violin plot to visualize billing amount distributions across different medical conditions.

**Purpose:** To understand the spread and distribution of hospital billing amounts for each medical condition.

### 4. Violin Plot – Billing by Insurance Provider

Compared billing amount distributions across insurance providers.

**Purpose:** To identify differences in billing distributions among insurance companies.

### 5. Monthly Patient Admission

Used a line chart to visualize the number of patient admissions for each month.

**Purpose:** To identify monthly admission trends and changes in patient volume.

### 6. Correlation Analysis

Calculated the correlation between:

* Age

* Hospital Stay Duration

* Billing Amount

#### Correlation Matrix

| Variables                      | Correlation |
| ------------------------------ | ----------- |
| Age & Stay Duration            | 0.008220    |
| Age & Billing Amount           | -0.003832   |
| Stay Duration & Billing Amount | -0.005602   |

**Observation:** The calculated correlations are close to zero, indicating very weak linear relationships between these numerical variables in this dataset.

### 7. Heatmap

Used a Seaborn heatmap to visualize the correlation matrix.

**Purpose:** To represent the relationships between numerical variables using colors and correlation values.

## Visualizations

The project includes:

1. Stacked Bar Chart – Average Billing by Medical Condition and Insurance Provider

2. Violin Plot – Billing Distribution by Medical Condition

3. Violin Plot – Billing Distribution by Insurance Provider

4. Line Chart – Monthly Patient Admissions

5. Heatmap – Correlation Matrix

## Key Findings

* The dataset contains 55,500 patient records and 15 columns.

* No missing values were identified.

* Hospital stay duration was calculated using admission and discharge dates.

* Billing amounts were analyzed across medical conditions and insurance providers.

* Monthly patient admissions were visualized using a line chart.

* Correlation values between age, stay duration, and billing amount are close to zero.

## How to Run the Project

1. Download the `healthcare_dataset.csv` file.

2. Open Google Colab or Jupyter Notebook.

3. Import the required Python libraries.

4. Load the dataset using Pandas.

5. Perform data inspection and preprocessing.

6. Execute the EDA and visualization code cells.

7. Analyze the generated charts and correlation matrix.

## Conclusion

This project demonstrates the use of Python for healthcare data analysis and visualization. Through data preprocessing, statistical analysis, and graphical representation, the project explores patient admissions, billing distributions, medical conditions, insurance providers, and relationships between numerical variables.


