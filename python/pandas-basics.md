---
layout: default
title: "Pandas Basics"
order: 79
---

Pandas is a library for data manipulation and analysis.

### Installing Pandas

Install using pip:

```plaintext
pip install pandas
```

### Creating a DataFrame

Example:

```python
import pandas as pd

data = {
    "Name": ["Alice", "Bob", "Charlie"],
    "Age": [25, 30, 35],
    "City": ["New York", "Los Angeles", "Chicago"]
}

df = pd.DataFrame(data)
print(df)
```

### Expected Output

```plaintext
      Name  Age         City
0    Alice   25     New York
1      Bob   30  Los Angeles
2  Charlie   35      Chicago
```

Pandas simplifies working with structured data.
