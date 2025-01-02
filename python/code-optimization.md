---
layout: default
title: "Code Optimization"
order: 101
---

Profiling identifies performance bottlenecks in your code. Python’s `cProfile` module is a powerful tool for this purpose.

### Profiling with cProfile

Example:

```python
import cProfile

def slow_function():
    total = 0
    for i in range(1, 1000000):
        total += i
    return total

cProfile.run("slow_function()")
```

### Optimizing with Time Complexity in Mind

Example:

```python
# Original code
squared = [x**2 for x in range(1000000)]

# Optimized code (generator expression)
squared = (x**2 for x in range(1000000))
```

### Expected Output

```plaintext
         4 function calls in 0.5 seconds
   ...
   1    0.5    0.5    0.5    0.5 <module>
```

Profiling helps you find inefficiencies and improve your code's performance.
