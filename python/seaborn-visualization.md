---
layout: default
title: "Seaborn Visualization"
order: 83
---

Seaborn is a statistical data visualization library built on top of Matplotlib.

### Installing Seaborn

Install using pip:

```plaintext
pip install seaborn
```

### Creating a Simple Plot

Example:

```python
import seaborn as sns
import matplotlib.pyplot as plt

data = [10, 20, 25, 30, 35, 40]
sns.histplot(data, kde=True)
plt.title("Histogram with KDE")
plt.show()
```

### Expected Output

A histogram with a KDE (Kernel Density Estimate) overlay.

Seaborn makes it easier to create visually appealing and informative plots.
