#**EXPERIMENT 13 : Data Preprocessing & Handling Missing Values**

##*AIM*: **To perform preprocessing on a dataset and Dealing with Missing Values** 

*THEORY*:
Data preprocessing is a crucial step in data analysis and machine learning. Real-world datasets often contain:
1. Missing values
2. Inconsistent formats
3. Incorrect data types
4. Duplicate or noisy data

Handling missing values is important because:

1. It improves data quality
2. Prevents errors during analysis
3. Enhances model performances
   
Common Techniques for Handling Missing Values:

Removing data: Row-wise deletion (dropna()) and Column-wise deletion

Replacing missing values: With constant values (e.g., 0, "DEFAULT") and With statistical measures like Mean, Mode and Median

Data Transformation: Converting data types and standardizing formats of dates and texts

1. Importing Libraries
pandas: Used for data manipulation
numpy: Used for numerical operations and handling NaN

2. Creating a DataFrame: A sample dataset is created with missing values (np.nan).

3. Detecting Missing Values - df1.isna(): Returns True where values are missing.
                            - df1.notna(): Returns True where values are present.

4. Counting Missing Values-
   
df1.isna().sum(): Counts missing values column-wise.

df1.isna().sum(axis=1): Counts missing values row-wise.





Standardizing formats (e.g., dates, text)
