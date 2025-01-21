---
title: "Introduction to Pandas"
order: 33
---

# Introduction to Pandas

Pandas is a powerful Python library for data manipulation and analysis. It provides data structures like **Series** and **DataFrame** to work efficiently with structured data.

---

## Installing Pandas

To use Pandas, install it via `pip`:

```bash
pip install pandas
```

---

## Core Data Structures

### 1. Series
A **Series** is a one-dimensional labeled array.

```python
import pandas as pd

# Creating a Series
data = [10, 20, 30]
series = pd.Series(data, index=["a", "b", "c"])

print(series)
# Output:
# a    10
# b    20
# c    30
# dtype: int64
```

### 2. DataFrame
A **DataFrame** is a two-dimensional labeled data structure.

```python
# Creating a DataFrame
data = {
    "Name": ["Alice", "Bob", "Charlie"],
    "Age": [25, 30, 35],
    "City": ["New York", "Los Angeles", "Chicago"]
}
df = pd.DataFrame(data)

print(df)
# Output:
#       Name  Age         City
# 0    Alice   25     New York
# 1      Bob   30  Los Angeles
# 2  Charlie   35      Chicago
```

---

## Reading and Writing Data

### Reading Data
Pandas supports reading data from various file formats:

- **CSV**:
  ```python
  df = pd.read_csv("data.csv")
  ```

- **Excel**:
  ```python
  df = pd.read_excel("data.xlsx")
  ```

- **JSON**:
  ```python
  df = pd.read_json("data.json")
  ```

### Writing Data
You can write a DataFrame to a file:

- **CSV**:
  ```python
  df.to_csv("output.csv", index=False)
  ```

- **Excel**:
  ```python
  df.to_excel("output.xlsx", index=False)
  ```

---

## Exploring Data

```python
# Display first few rows
print(df.head())

# Display last few rows
print(df.tail())

# Summary of the DataFrame
print(df.info())

# Statistical summary
print(df.describe())
```

---

## Selecting and Filtering Data

### Selecting Columns
```python
# Single column
print(df["Name"])

# Multiple columns
print(df[["Name", "City"]])
```

### Filtering Rows
```python
# Rows where Age > 30
print(df[df["Age"] > 30])

# Rows where City is Chicago
print(df[df["City"] == "Chicago"])
```

### Using Conditions
```python
# Multiple conditions
print(df[(df["Age"] > 25) & (df["City"] == "New York")])
```

---

## Modifying Data

### Adding a Column
```python
df["Salary"] = [50000, 60000, 70000]
print(df)
```

### Updating Values
```python
df.loc[0, "Age"] = 26
print(df)
```

### Removing Columns and Rows
```python
# Remove a column
df = df.drop("Salary", axis=1)

# Remove a row
df = df.drop(0, axis=0)
```

---

## Grouping and Aggregating Data

### Grouping
```python
grouped = df.groupby("City")
print(grouped["Age"].mean())
```

### Aggregating
```python
print(df.groupby("City").agg({"Age": ["mean", "max"]}))
```

---

## Merging and Joining DataFrames

### Merging
```python
df1 = pd.DataFrame({"ID": [1, 2], "Name": ["Alice", "Bob"]})
df2 = pd.DataFrame({"ID": [1, 2], "Score": [85, 90]})

merged = pd.merge(df1, df2, on="ID")
print(merged)
```

### Concatenating
```python
df1 = pd.DataFrame({"Name": ["Alice", "Bob"]})
df2 = pd.DataFrame({"Name": ["Charlie", "David"]})

concat = pd.concat([df1, df2])
print(concat)
```

---

## Handling Missing Data

### Identifying Missing Data
```python
print(df.isnull())
print(df.isnull().sum())
```

### Filling Missing Data
```python
df["Age"].fillna(30, inplace=True)
```

### Dropping Missing Data
```python
df.dropna(inplace=True)
```

---

## Practical Examples

### Calculate Average Salary
```python
print("Average Salary:", df["Salary"].mean())
```

### Count Unique Cities
```python
print("Unique Cities:", df["City"].nunique())
```

### Sort by Age
```python
df = df.sort_values(by="Age", ascending=False)
print(df)
```

---

## Practice Exercises

1. **Read a CSV**:
   - Load a CSV file into a DataFrame and display the first 5 rows.

2. **Filter Data**:
   - Find all rows where the age is greater than 30.

3. **Group and Aggregate**:
   - Group data by a column and calculate the average of another column.

4. **Handle Missing Data**:
   - Identify missing values in a dataset and fill them with a default value.

5. **Merge DataFrames**:
   - Merge two DataFrames on a common column.

Pandas is an essential library for anyone working with data in Python. Mastering its features will enable you to handle, analyze, and visualize data efficiently.