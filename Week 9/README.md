# Real Estate Valuation – Data Cleaning and Feature Engineering

## Project Overview
This project focuses on cleaning and analyzing real estate data using Python. The dataset contains house prices, bedrooms, bathrooms, living area, lot area, construction year, renovation year, and geographical coordinates.

The main goal is to prepare the data, create new features, calculate price per square foot, and identify house price outliers.

## Objectives
- Inspect property features such as bedrooms, bathrooms, living area, and grade.
- Clean missing values and remove duplicate records.
- Handle invalid zero values in bedroom and bathroom counts.
- Extract sale year from the date column.
- Calculate property age and renovation status.
- Calculate price per square foot for living area and lot size.
- Identify house price outliers using box plots and statistical bounds.

## Dataset
**Dataset Name:** kc_house_data.csv

**Total Records:** 21,613

**Total Columns:** 21

### Important Features
- `price` – House selling price
- `bedrooms` – Number of bedrooms
- `bathrooms` – Number of bathrooms
- `sqft_living` – Living area in square feet
- `sqft_lot` – Lot size in square feet
- `grade` – House construction and design grade
- `yr_built` – Year the house was built
- `yr_renovated` – Year the house was renovated
- `date` – House sale date
- `lat` and `long` – Geographical coordinates

## Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Google Colab

## Project Workflow

### 1. Data Loading
Load the real estate dataset using Pandas.

### 2. Data Inspection
Inspect the dataset using `head()`, `tail()`, `info()`, `describe()`, and `shape`.

### 3. Data Cleaning
- Check missing values.
- Remove duplicate records.
- Remove invalid zero values in bedroom and bathroom counts.
- Prepare the dataset for analysis.

### 4. Feature Engineering
- Extract `Sale_Year` from the date column.
- Calculate `Property_Age`.
- Create `Is_Renovated`.
- Calculate `Price_Per_Sqft_Living`.
- Calculate `Price_Per_Sqft_Lot`.

### 5. Outlier Detection
Use a box plot to visualize house price outliers.

Calculate Q1, Q3, IQR, lower bound, and upper bound using the IQR method.

Identify house prices outside the statistical bounds.

## Features Created

| Feature | Description |
|---|---|
| Sale_Year | Year of house sale |
| Property_Age | Age of the house at sale |
| Is_Renovated | Renovation status (1 or 0) |
| Price_Per_Sqft_Living | Price divided by living area |
| Price_Per_Sqft_Lot | Price divided by lot size |

## Expected Results
- Cleaned real estate dataset.
- Property age and renovation status features.
- Price per square foot calculations.
- Box plot showing house price distribution.
- Statistical bounds for identifying outliers.

## Conclusion
This project uses Python for real estate data cleaning, feature engineering, and outlier detection. The created features help understand house characteristics, property age, renovation status, and price variation. Statistical bounds and box plots help identify extreme house prices.
