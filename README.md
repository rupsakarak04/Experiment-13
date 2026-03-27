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

**1. Importing Libraries**
pandas: Used for data manipulation
numpy: Used for numerical operations and handling NaN

**2. Creating a DataFrame:** A sample dataset is created with missing values (np.nan).

**3. Detecting Missing Values**

df1.isna(): Returns True where values are missing.
                        
df1.notna(): Returns True where values are present.

**4. Counting Missing Values**
   
df1.isna().sum(): Counts missing values column-wise.

df1.isna().sum(axis=1): Counts missing values row-wise.

**5. Removing Missing Values**
   
df1.dropna(): Drops rows containing missing values.

df1.dropna(axis=1): Drops columns containing missing values.

**6. Filling Missing Values**

df1.fillna(value='DEFAULT'): Replaces missing values with a string.

df1.fillna(0): Replaces missing values with zero.

df1.fillna(df1.mean()): Replaces missing values with column mean.

df1.apply(lambda row: row.fillna(row.mean()), axis=1): Replaces missing values using row-wise mean.

**Step 1:** Replace Invalid Values

df.replace("-", np.nan, inplace=True): Converts "-" into NaN to mark missing data.

**Step 2:** Convert Data Types

df["Age"] = pd.to_numeric(df["Age"], errors='coerce')

df["Marks"] = pd.to_numeric(df["Marks"], errors='coerce')

Converts columns to numeric.

Invalid values become NaN.

**Step 3:** Handle Missing Values

df["Age"].fillna(df["Age"].mean(), inplace=True)

df["Marks"].fillna(df["Marks"].median(), inplace=True)

Age → filled with mean

Marks → filled with median

**Step 4:** Fix Text Formatting

df["Department"] = df["Department"].str.upper(): Converts all text to uppercase for consistency.

**Step 5:** Convert Date Format

df["Admission_Date"] = pd.to_datetime(df["Admission_Date"], format='mixed', dayfirst=True): Converts date column into standard datetime format.

*CONCLUSION:*

In this experiment, we successfully Identified missing values using isna(), Removed unwanted data using dropna(), Replaced missing values using mean, median, and constants, Cleaned inconsistent data formats, Converted data types for proper analysis, Standardized text and date formats. Overall, data preprocessing improves the accuracy, consistency, and usability of the dataset, making it ready for further analysis or machine learning tasks.




















