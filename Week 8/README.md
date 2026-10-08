# WEEK-8 
# Student Performance Analysis
## Project Overview

This project analyzes student performance data to understand how different factors affect students' academic scores.

The analysis focuses on:

Parental education level
Lunch type
Test preparation course
Math score
Reading score
Writing score

The project uses Python, Pandas, Matplotlib, and Seaborn for data analysis and visualization.

## Dataset

Dataset: studentperformance_preprocessed.csv

The dataset contains 1000 student records and the following columns:

Column	Description
gender	Gender of the student
race/ethnicity	Student's race/ethnicity group
parental level of education	Education level of the student's parents
lunch	Type of lunch received
test preparation course	Whether the student completed test preparation
math score	Math test score
reading score	Reading test score
writing score	Writing test score

## Objectives
Compare average test scores across different parental education levels and lunch types.
Analyze score variation between students who completed test preparation and those who did not.
Study the relationship between Math and Reading scores.
Study the relationship between Math and Writing scores.
Evaluate correlations between Math, Reading, and Writing scores.
Identify factors that may influence student performance.
Provide educational equity and policy recommendations.

## Technologies Used
Python
Pandas – Data loading and analysis
Matplotlib – Data visualization
Seaborn – Statistical visualization
Google Colab / Jupyter Notebook – Development environment

## Visualizations
1. Grouped Bar Chart

A grouped bar chart is used to compare the average Math score based on:

Parental education level
Lunch type

This helps identify differences in student performance across different groups.

2. Box Plot

A box plot is used to compare Math score distributions between students who:

Completed the test preparation course
Did not complete the test preparation course

It helps identify the median, spread, and possible outliers.

3. Scatter Plot – Math vs Reading

This plot shows the relationship between Math and Reading scores.

A positive relationship indicates that students with higher Math scores generally tend to have higher Reading scores.

4. Scatter Plot – Math vs Writing

This plot shows the relationship between Math and Writing scores.

It helps understand whether performance in Math is related to performance in Writing.

5. Correlation Heatmap

The correlation heatmap shows the relationship between:

Math Score
Reading Score
Writing Score

Correlation values range from -1 to +1.

+1 → Strong positive relationship
0 → No relationship
-1 → Strong negative relationship

## Key Analysis

The project evaluates how student performance varies according to parental education, lunch type, and test preparation.

It also examines whether performance in one subject is related to performance in another subject.

The visualizations make it easier to identify patterns and differences that may not be obvious from the raw dataset.

## Conclusion

This project provides a visual and statistical analysis of student performance. The use of bar charts, box plots, scatter plots, and correlation heatmaps helps understand 
the factors associated with academic performance.

The analysis can help educators identify performance gaps and develop strategies to provide equal educational opportunities and better academic support for students.
