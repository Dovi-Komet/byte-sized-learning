---
layout: default
title: "CSV Files"
order: 69
---

Python's `csv` module makes it easy to work with CSV files.

### Reading a CSV File

Example:

```python
import csv

with open("example.csv", mode="r") as file:
    reader = csv.reader(file)
    for row in reader:
        print(row)
```

### Expected Output (based on file content)

```plaintext
['Name', 'Age']
['Alice', '25']
['Bob', '30']
```

### Writing to a CSV File

Example:

```python
with open("output.csv", mode="w", newline="") as file:
    writer = csv.writer(file)
    writer.writerow(["Name", "Age"])
    writer.writerow(["Charlie", "35"])
```

CSV files are widely used for data storage and transfer.
