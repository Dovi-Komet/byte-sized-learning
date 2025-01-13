---
layout: default
title: "Error Handling Basics"
order: 29
---

Errors and exceptions are inevitable when writing code. Python provides mechanisms to handle these situations gracefully, ensuring that your program doesn’t crash unexpectedly.

## What Is Error Handling?

Error handling involves catching and managing errors that occur during program execution. Python uses `try`, `except`, `else`, and `finally` blocks to handle errors.

---

## The `try` and `except` Blocks

The `try` block contains code that might raise an error, and the `except` block specifies how to handle the error.

### Example:
```python
try:
    num = int(input("Enter a number: "))
    print(f"You entered: {num}")
except ValueError:
    print("That's not a valid number!")
```

### Output (if input is invalid):
```plaintext
Enter a number: abc
That's not a valid number!
```

---

## Using `else` for Success

The `else` block runs if no errors occur in the `try` block.

### Example:
```python
try:
    num = int(input("Enter a number: "))
except ValueError:
    print("Invalid input!")
else:
    print(f"You entered the number {num}")
```

### Output:
If valid input is provided:
```plaintext
Enter a number: 5
You entered the number 5
```

If invalid input is provided:
```plaintext
Enter a number: xyz
Invalid input!
```

---

## The `finally` Block

The `finally` block always runs, regardless of whether an error occurred. It’s commonly used for cleanup tasks.

### Example:
```python
try:
    file = open("example.txt", "r")
    content = file.read()
    print(content)
except FileNotFoundError:
    print("File not found!")
finally:
    print("Execution completed.")
```

### Output (if file does not exist):
```plaintext
File not found!
Execution completed.
```

---

## Catching Multiple Exceptions

You can handle different types of exceptions using multiple `except` blocks.

### Example:
```python
try:
    num = int(input("Enter a number: "))
    result = 10 / num
except ValueError:
    print("Invalid input! Please enter a number.")
except ZeroDivisionError:
    print("Cannot divide by zero.")
```

### Output:
If invalid input:
```plaintext
Enter a number: abc
Invalid input! Please enter a number.
```

If dividing by zero:
```plaintext
Enter a number: 0
Cannot divide by zero.
```

---

Error handling is a fundamental skill for writing robust programs. In the next lesson, we’ll dive deeper into Python’s exception handling capabilities.
