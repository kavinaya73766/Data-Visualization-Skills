# Task 2 – Big Data Analysis
## Project Overview
This project focuses on performing data analysis and exploratory data visualization using the Sample Superstore dataset.

The main objective is to understand sales, profit, discount, delivery time, category-wise performance, and relationships between numerical variables using Python and popular data analysis libraries.

## Objectives
Load and inspect the Superstore dataset.
Perform basic data preprocessing.
Convert date columns into proper datetime format.
Calculate delivery time in days.
Check for missing values.
Analyze sales and profit by category.
Study the distribution of sales and profit.
Analyze the relationship between discount and profit.
Generate a correlation matrix and heatmap.
Visualize important business insights using graphs.

## Technologies Used
Python
Pandas
NumPy
Matplotlib
Seaborn
Google Colab
Jupyter Notebook

## Dataset
Dataset: Sample Superstore Dataset

The dataset contains business transaction information such as:

Order Date
Ship Date
Category
Sales
Profit
Discount
Other numerical and categorical attributes


## Exploratory Data Analysis
##  Import Libraries

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

*Purpose:* Imports libraries required for data analysis and visualization.

---

##  Load Dataset

```python
python
from google.colab import drive
drive.mount('/content/drive')
```

```python
df = pd.read_csv("/content/drive/MyDrive/BIG DATA /SuperStore.csv.csv")
```

*Purpose:* Connects Google Drive and loads the SuperStore dataset into a DataFrame.

---

## Initial Data Exploration

```python
### df.head()
```

Displays the first 5 rows to understand the dataset structure.

```python
### df.info()
```

Checks rows, columns, data types, and non-null values.

*Result:* Dataset contains *1000 records and 26 columns*.

```python
### df.describe()
```

Provides statistical information such as mean, minimum, maximum, and standard deviation.

---

##  Date Conversion

```python
python
df['Order Date'] = pd.to_datetime(df['Order Date'])
df['Ship Date'] = pd.to_datetime(df['Ship Date'])
```

*Purpose:* Converts date columns into datetime format for date calculations.

---

##  Delivery Days

```python
python
df['Delivery Days'] = (
    df['Ship Date'] - df['Order Date']
).dt.days
```

*Purpose:* Calculates the number of days taken to ship each order.

A new column called *Delivery Days* is added.

---

##  Missing Value Check

```python
python
df.isnull().sum()
```

*Purpose:* Checks for missing values.

*Result:* All columns have *0 missing values*, so no missing-value treatment is required.

---

#  Data Visualization & Analysis

## A. Sales by Category – Bar Plot

```python
python
category_sales = df.groupby(
    'Category'
)['Sales Amount'].sum()

category_sales.plot(kind='bar')
```

*Purpose:* Compares total sales between product categories.

### Analysis

* Office Supplies has the *highest total sales*.
* Furniture has the *lowest total sales* among the four categories.
* Sales performance is relatively close across the categories.

*Insight:* Office Supplies is the strongest category in terms of total sales.

---

## B. Sales Distribution – Histogram

```python
python
sns.histplot(df['Sales Amount'], bins=30)
```

*Purpose:* Shows how sales values are distributed.

### Analysis

Most orders are concentrated in the lower-to-middle sales ranges, while a smaller number of orders have very high sales values.

*Insight:* Sales are not evenly distributed; some high-value orders contribute significantly to total sales.

---

## C. Profit by Category – Bar Plot

```python
python
sns.barplot(
    data=df,
    x="Category",
    y="Profit"
)
```

*Purpose:* Compares the average profit across categories.

### Analysis

The graph shows differences in average profit between product categories.

*Insight:* Some categories generate better profit per order even when their total sales are not the highest.

---

## D. Sales by Category – Bar Plot

```python
python
sns.barplot(
    data=df,
    x="Category",
    y="Sales"
)
```

*Purpose:* Compares sales values across categories.

### Analysis

The categories show similar sales performance, with Office Supplies performing strongly.

*Insight:* No single category completely dominates sales; performance is distributed across categories.

---

## E. Profit Distribution – Box Plot

```python
python
sns.boxplot(data=df, y="Profit")

```

*Purpose:* Understands the overall distribution of profit.

### Analysis

The box plot shows the median, spread, and possible high-profit outliers.

*Insight:* Profit varies considerably between orders, with some orders generating much higher profit than typical orders.

---

## F. Profit Variation Across Categories – Box Plot

```python
python
sns.boxplot(
    data=df,
    x="Category",
    y="Profit"
)
```

*Purpose:* Compares profit variation between categories.

### Analysis

The categories have different median profits and profit spreads. Some categories also contain higher-value profit observations.

*Insight:* Profitability is not uniform across product categories.

---

## G. Discount Values

```python
python
df["Discount (%)"].unique()
```

*Result:*

text
0%, 5%, 10%, 15%, 20%


*Purpose:* Identifies the different discount levels used in the dataset.

---

## H. Discount vs Profit – Scatter Plot

```python
python
sns.scatterplot(
    data=df,
    x="Discount (%)",
    y="Profit"
)
```

*Purpose:* Studies the relationship between discount and profit.

### Analysis

The points are widely scattered and do not show a strong clear pattern.

The correlation is approximately *-0.080*.

*Insight:* Discount has a *very weak negative relationship* with profit in this dataset.

---

#  Correlation Analysis

## Selecting Numerical Columns

```python
python
numeric_df = df.select_dtypes(include="number")
```

*Purpose:* Selects numerical columns for correlation analysis.

---

## Correlation Matrix

```python
python
corr = numeric_df.corr()
```

*Purpose:* Measures relationships between numerical variables.

### Important Findings

| Relationship                  | Correlation | Analysis               |
| ----------------------------- | ----------: | ---------------------- |
| Sales Amount – Profit         |       0.868 | Strong positive        |
| Sales Amount – Cost Price     |       0.984 | Very strong positive   |
| Quantity – Sales Amount       |       0.620 | Moderate positive      |
| Stock Left – Reorder Quantity |      -0.663 | Moderate negative      |
| Discount – Profit             |      -0.080 | Very weak negative     |
| Delivery Days – Profit        |       0.022 | Almost no relationship |

---

#  Correlation Heatmap

```python
python
sns.heatmap(corr, annot=True)
```

*Purpose:* Displays all numerical correlations visually.

### Analysis

The heatmap clearly shows that:

* *Sales Amount and Profit* have a strong positive relationship.
* *Sales Amount and Cost Price* have a very strong relationship.
* *Stock Left and Reorder Quantity* have a negative relationship.
* *Discount and Profit* have very little relationship.
* *Delivery Days* has very little relationship with sales and profit

## Visualizations
The project includes the following visualizations:

Sales by Category
Sales Distribution Histogram
Profit by Category
Sales Distribution by Category
Profit Distribution Box Plot
Profit Variation Across Categories
Discount vs Profit Scatter Plot
Correlation Heatmap


## Sales by Category
<img width="1011" height="708" alt="image" src="https://github.com/user-attachments/assets/5d9271e1-f1b5-48c5-9cbf-92ad10e3f4ad" />

## Sales Distribution Histogram
<img width="1027" height="606" alt="image" src="https://github.com/user-attachments/assets/754b3167-59f2-48cc-b59b-3791ca2565a7" />

## Profit by category
<img width="842" height="585" alt="image" src="https://github.com/user-attachments/assets/f5f09757-a149-4bd3-b1c4-23e0aa6f9823" />

## Sales Distribution by category
<img width="765" height="590" alt="image" src="https://github.com/user-attachments/assets/b68d1514-36f8-4edf-87a5-7a6196b22b8c" />

## Profit Distribution
<img width="887" height="533" alt="image" src="https://github.com/user-attachments/assets/49fe2813-4246-456a-870e-1db9fff91b4b" />

## Profit variation Across Categories
<img width="840" height="583" alt="image" src="https://github.com/user-attachments/assets/7b11af53-b512-4cb2-8257-c65fb35d7336" />

## Discount vs profit Scatter plot
<img width="813" height="580" alt="image" src="https://github.com/user-attachments/assets/7d4249c9-f8f3-411c-ad2c-8fb05841d554" />

## Correlation Heatmap
<img width="773" height="657" alt="image" src="https://github.com/user-attachments/assets/f9298e53-a4e3-4a82-bed0-e7b3e7419965" />


## Key Analysis Areas
The analysis focuses on:

Sales Analysis

Category-wise sales performance
Overall sales distribution
Profit Analysis

Category-wise profit
Profit variation and distribution
Discount Analysis

Relationship between discount and profit
Delivery Analysis

Number of days between order and shipping
Correlation Analysis

Relationships among numerical variables

## Project Structure

Task-2-BD/
│
├── Task_2_BD.ipynb
├── task_2_bd.py
└── README.md

## How to Run

Using Google Colab
Open Task_2_BD.ipynb.
Upload the Sample Superstore CSV dataset.
Update the dataset path if required.
Run all cells sequentially.
Using Jupyter Notebook
Install the required libraries:

pip install pandas numpy matplotlib seaborn
Then open:

Task_2_BD.ipynb
and execute the cells.

## Conclusion

This project demonstrates the use of Python-based data analysis and visualization techniques on the Sample Superstore dataset. The analysis helps understand sales, profit, discount, delivery time, category performance, and correlations between numerical variables.

The project provides a basic foundation for performing Exploratory Data Analysis (EDA) and extracting useful insights from business data.
