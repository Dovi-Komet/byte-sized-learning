---
layout: default
title: "Multiple Exceptions"
order: 29
---

In Python, you can handle multiple types of exceptions using multiple `except` blocks.

### Handling Specific Exceptions

You can specify different actions for different types of errors.

Example:

```python
try:
    number = int(input("Enter a number: "))
    result = 10 / number
    print("Result is:", result)
except ValueError:
    print("That's not a valid number!")
except ZeroDivisionError:
    print("Cannot divide by zero!")
```

### Expected Output (if the user enters `0`)

```plaintext
Cannot divide by zero!
```

### Expected Output (if the user enters `abc`)

```plaintext
That's not a valid number!
```

This ensures your program handles each type of error appropriately.