# Healthcare Dataset Analysis 🏥

## Project Overview

This project performs **data understanding, cleaning, and basic analysis** on a healthcare dataset using Python.

The analysis focuses on patient admission information, admission types, medical codes, dates, hospital stay duration, and billing amounts.

## Technologies Used

* Python
* Pandas
* Matplotlib
* Seaborn
* Google Colab

## Dataset

The project uses a **Healthcare Dataset** containing patient and hospital-related information.

Some of the columns used in the analysis include:

* `Medical_Code`
* `Admission_Date`
* `Discharge_Date`
* `Admission_Type`
* `Billing_Amount`

##  Data Analysis Performed

The notebook performs the following operations:

1. Import required Python libraries.
2. Load the healthcare dataset using Pandas.
3. Display the first few records.
4. Check the column names.
5. Check the number of rows and columns.
6. Check the data types.
7. Check for missing values.
8. Check missing values in the `Medical_Code` column.
9. Convert `Admission_Date` into datetime format.
10. Convert `Discharge_Date` into datetime format.
11. Analyze the different admission types.
12. Convert `Admission_Type` values into lowercase.
13. Generate descriptive statistics using `describe()`.
14. Calculate the number of hospital stay days.
15. Analyze the `Billing_Amount` column using descriptive statistics.

## Feature Engineering

A new column called `Hospital_Stay_Days` is created using the admission and discharge dates.

```python
df["Hospital_Stay_Days"] = (
    df["Discharge_Date"] - df["Admission_Date"]
).dt.days
```

This calculates the number of days each patient stayed in the hospital.

## Data Cleaning

The following data-cleaning operations are performed:

* Checking for missing values.
* Checking missing values in `Medical_Code`.
* Converting admission dates to datetime format.
* Converting discharge dates to datetime format.
* Standardizing `Admission_Type` values by converting them to lowercase.

## Statistical Analysis

Descriptive statistics are calculated for the dataset and for the `Billing_Amount` column.

```python
df.describe()

df["Billing_Amount"].describe()
```

These statistics help understand the numerical characteristics of the healthcare data.

## Project Structure

```text
Healthcare-Dataset-Analysis/
│
├── week_5.ipynb
├── healthcare_dataset.csv
└── README.md
```

## Objective

The main objective of this project is to understand and prepare healthcare data for further analysis by checking its structure, identifying missing values, converting date columns, standardizing categorical data, calculating hospital stay duration, and analyzing billing amounts.

## Conclusion

This project demonstrates how **Pandas** can be used for healthcare data analysis. The dataset is inspected and cleaned, date columns are converted into the correct format, admission types are standardized, hospital stay duration is calculated, and billing amount statistics are analyzed.
