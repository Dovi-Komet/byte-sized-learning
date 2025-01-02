---
layout: default
title: "The finally Block"
order: 30
---

The `finally` block allows you to execute code regardless of whether an error occurs or not.

### Using `finally`

Example:

```python
try:
    file = open("example.txt", "r")
    content = file.read()
    print(content)
except FileNotFoundError:
    print("File not found.")
finally:
    print("Execution completed.")
```

### Expected Output (if `example.txt` does not exist)

```plaintext
File not found.
Execution completed.
```

The `finally` block is useful for cleanup tasks like closing files or releasing resources.