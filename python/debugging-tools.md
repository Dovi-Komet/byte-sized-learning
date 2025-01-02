---
layout: default
title: "Debugging Tools"
order: 95
---

Debugging is essential for resolving issues in your code. This lesson covers tools like `pdb` and logging levels.

### Debugging with pdb

Python's built-in debugger, `pdb`, allows you to pause code execution and inspect variables.

Example:

```python
def buggy_function(a, b):
    import pdb; pdb.set_trace()  # Pause here
    result = a / b
    return result

print(buggy_function(10, 0))
```

### Using Logging Levels

The `logging` module offers levels like `DEBUG`, `INFO`, `WARNING`, `ERROR`, and `CRITICAL`.

Example:

```python
import logging

logging.basicConfig(level=logging.DEBUG)

def calculate_sum(a, b):
    logging.debug(f"Adding {a} and {b}")
    return a + b

print(calculate_sum(5, 7))
```

### Expected Output

```plaintext
DEBUG:root:Adding 5 and 7
12
```

Debugging tools make diagnosing and fixing issues efficient.
