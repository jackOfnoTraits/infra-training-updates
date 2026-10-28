# DC-26: Day 11 - Task 3 - E-Commerce Data Cleaning and Preprocessing

- **Jira:** https://lakshmibanka516.atlassian.net/browse/DC-26
- **Status:** Done
- **Assignee:** sasidharana504
- **Issue type:** Task
- **Priority:** Medium
- **Resolution:** Done
- **Reporter:** sasidharana504
- **Created:** 2026-10-27T10:59:01.756Z
- **Updated:** 2026-10-28T04:39:55.500Z
- **Due date:** —
- **Labels:** —
- **Components:** —

## Description

Labels: data-cleaning, data-preprocessing, e-commerce

Description

Select a unique e-commerce dataset from a public source and perform basic data cleaning and preprocessing using Python and Pandas. Identify data quality issues, clean the dataset, and perform simple business analysis.

Tasks and Commands

1. Select and Inspect a Dataset

- Download a unique e-commerce dataset from Kaggle, UCI, or GitHub.
- Load the dataset and inspect its structure.

```
import pandas as pd

df = pd.read_csv("ecommerce.csv")

print(df.head())
print(df.shape)
print(df.info())
```

2. Identify Missing Values

- Find missing values in every column.
- Count missing values and handle them appropriately.

```
print(df.isnull().sum())
print(df.isnull().sum() / len(df) * 100)

# Remove rows with missing values, if appropriate
df = df.dropna()
```

3. Identify and Remove Duplicate Orders

- Find repeated order IDs.
- Check whether they represent actual duplicates or legitimate items belonging to the same order.
- Remove only confirmed duplicate records.

```
print(df["OrderID"].duplicated().sum())

# Remove exact duplicate rows
df = df.drop_duplicates()
```

Replace OrderID with the actual order ID column name in your dataset.

4. Find the Highest-Priced Product

- Identify the product with the highest valid unit price.
- Display its name and price.

```
print(df.loc[df["UnitPrice"].idxmax()])
```

5. Calculate Revenue by City

- Calculate revenue using quantity multiplied by unit price.
- Group revenue by city and identify the highest-revenue city.

```
df["Revenue"] = df["Quantity"] * df["UnitPrice"]

city_revenue = df.groupby("City")["Revenue"].sum()

print(city_revenue.sort_values(ascending=False))
```

6. Identify Possible Causes and Solutions

Document the possible causes and solutions for the following issues:

- Missing values — incomplete data entry or failed imports.
- Duplicate records — repeated uploads or transactions.
- Invalid prices — data entry errors or incorrect formats.
- Inconsistent city names — spelling differences or inconsistent formatting.
Suggest a suitable solution for each issue.

7. Save the Cleaned Dataset

- Save the final dataset as a CSV file.
- Submit the notebook and a brief summary of findings.

```
df.to_csv("cleaned_ecommerce.csv", index=False)
```

Deliverables

- Original dataset and source link.
- Python notebook (.ipynb).
- Cleaned dataset (.csv).
- Results of the analyses and suggested solutions.
Tools: Python, Pandas, Jupyter Notebook.

Estimated effort: 2–3 hours per member.

## Attachments

- [Day-11-Task-3.html](attachments/Day-11-Task-3.html)
- [Day-11-Task-3.ipynb](attachments/Day-11-Task-3.ipynb)
