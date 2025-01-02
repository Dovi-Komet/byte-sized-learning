---
layout: default
title: "Matplotlib Basics"
order: 78
---

Matplotlib is a powerful library for creating visualizations.

### Installing Matplotlib

Install using pip:

```plaintext
pip install matplotlib
```

### Basic Plot

Example:

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4]
y = [10, 20, 25, 30]

plt.plot(x, y)
plt.title("Basic Plot")
plt.xlabel("X-Axis")
plt.ylabel("Y-Axis")
plt.show()
```

### Expected Output

A simple line plot with labeled axes.

Matplotlib is great for creating a variety of 2D plots.
