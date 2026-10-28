# DC-22: Day 11 - Task 2 -  Data Cleaning, Preprocessing & Validation Using Pandas

- **Jira:** https://lakshmibanka516.atlassian.net/browse/DC-22
- **Status:** Done
- **Assignee:** sasidharana504
- **Issue type:** Task
- **Priority:** Medium
- **Resolution:** Done
- **Reporter:** sasidharana504
- **Created:** 2026-10-27T10:55:45.754Z
- **Updated:** 2026-10-28T04:38:53.198Z
- **Due date:** —
- **Labels:** —
- **Components:** —

## Description

Description

Practice the complete data preprocessing workflow using Python and Pandas, from inspecting raw data to cleaning, transforming, and validating the results.

Tasks

1. Load and Inspect Data  - Load the dataset into a Pandas DataFrame. - Inspect the first few rows using df.head(). - Check dataset dimensions using df.shape. - Examine column names, data types, and non-null counts using df.columns and df.info(). - Generate descriptive statistics using df.describe().
2. Identify and Handle Data Quality Issues  - Identify missing values using df.isnull().sum(). - Detect duplicate records using df.duplicated().sum() and remove them using df.drop_duplicates(). - Clean inconsistent string values using .str.strip().str.title(). - Convert date columns using pd.to_datetime() with errors="coerce". - Convert numeric columns using pd.to_numeric() with errors="coerce". - Inspect column data types using .dtype and identify invalid values introduced during conversion.
3. Detect and Handle Outliers  - Calculate Q1, Q3, and IQR for the UnitPrice column. - Calculate the lower and upper bounds using the IQR method:  - IQR = Q3 − Q1 - Lower Bound = Q1 − 1.5 × IQR - Upper Bound = Q3 + 1.5 × IQR - Identify potential outliers using these bounds. - Validate the results using df.plot(kind="box").
4. Transform and Enrich Data  - Create a new column by aggregating values from multiple existing columns. - Write a custom function to categorize values, such as assigning price categories (High, Low, Unknown, etc.) based on price. - Apply the function to create a new DataFrame column. - Explore additional useful Pandas operations for data cleaning and transformation.
5. Validate Final Results  - Recheck missing values, duplicate records, data types, and invalid values. - Verify that the new columns contain the expected results. - Compare the cleaned dataset with the original to ensure transformations are correct.
Expected Outcome

A cleaned and validated Pandas DataFrame with consistent values, appropriate data types, identified outliers, and additional derived columns.

## Attachments

- [Day-11-Task-2.html](attachments/Day-11-Task-2.html)
- [Day-11-Task-2.ipynb](attachments/Day-11-Task-2.ipynb)
