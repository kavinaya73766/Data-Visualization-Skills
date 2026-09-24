# Apple Stock Data Analysis 

##  Project Overview

This project performs basic **data analysis on Apple (AAPL) stock market data** using Python and the Pandas library.

The dataset contains stock information such as **Open, Close, High, and Low prices**. The project focuses on understanding the dataset, checking its structure, removing duplicate records, and calculating basic statistical values.

##  Technologies Used

* Python
* Pandas
* Google Colab
* CSV Dataset

##  Dataset

The project uses an **AAPL.csv** dataset containing Apple stock market data.

Important columns used in the analysis:

* `Open` – Opening stock price
* `Close` – Closing stock price
* `High` – Highest stock price
* `Low` – Lowest stock price

##  Analysis Performed

The following steps are performed in the notebook:

1. Import the Pandas library.
2. Load the `AAPL.csv` dataset.
3. Display the first few records using `head()`.
4. Display the last few records using `tail()`.
5. Check the dataset information using `info()`.
6. Check the data types of columns.
7. Display the column names.
8. Remove duplicate records.
9. Calculate the mean of the `Open` price.
10. Calculate the mean of the `Close` price.
11. Find the maximum `High` price.
12. Find the minimum `Low` price.

##  Statistical Analysis

The project calculates:

| Measure | Column |
| ------- | ------ |
| Mean    | Open   |
| Mean    | Close  |
| Maximum | High   |
| Minimum | Low    |

##  Sample Code

```python
import pandas as pd

df = pd.read_csv("AAPL.csv")

# Display first records
df.head()

# Display last records
df.tail()

# Dataset information
df.info()

# Column data types
df.dtypes

# Column names
df.columns

# Remove duplicate records
df = df.drop_duplicates()

# Statistical calculations
df["Open"].mean()
df["Close"].mean()
df["High"].max()
df["Low"].min()
```

##  Objective

The main objective of this project is to understand and analyze **Apple stock price data** using Pandas and perform basic data cleaning and statistical analysis.

##  Project Structure

```text
AAPL-Stock-Analysis/
│
├── APP.ipynb
├── AAPL.csv
└── README.md
```

##  Conclusion

This project demonstrates how **Pandas** can be used to load, inspect, clean, and analyze stock market data. It provides basic statistical information about Apple's stock prices and helps in understanding the structure and characteristics of the dataset.

You can save this as **`README.md`** and place it inside the same GitHub folder as `APP.ipynb` and `AAPL.csv`.
