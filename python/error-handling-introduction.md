---
layout: default
title: "Error Handling: Introduction"
order: 25
---

Error handling allows you to deal with errors gracefully and prevent your program from crashing.

### Using `try` and `except`

Use the `try` block to write code that might cause an error and the `except` block to handle the error.

Example:

```python
try:
    number = int(input("Enter a number: "))
    print("You entered:", number)
except ValueError:
    print("That's not a valid number!")
```

### Expected Output (if the user enters "abc")

```plaintext
That's not a valid number!
```

### Why Handle Errors?

Error handling ensures that your program can continue running even when unexpected inputs or situations occur.