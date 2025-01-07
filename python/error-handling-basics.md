---
layout: default
title: "Error Handling Basics"
order: 29
---

Error handling allows you to manage errors gracefully, ensuring your program doesn't crash unexpectedly. It also helps improve user experience by providing meaningful feedback during errors.

## Using `try` and `except`

Use the `try` block to write code that might cause an error, and the `except` block to handle the error if it occurs.

### Example: Handling Input Errors

```python
try:
    number = int(input("Enter a number: "))
    print("You entered:", number)
except ValueError:
    print("That's not a valid number!")
```

### Output (if the user enters `"abc"`)

```plaintext
That's not a valid number!
```

In this example:
- If the user enters something that cannot be converted to an integer, a `ValueError` occurs.
- The `except` block catches the error and provides a user-friendly message.

## Catching Multiple Exceptions

You can handle different types of errors by specifying multiple `except` blocks.

### Example: Handling Multiple Errors

```python
try:
    number = int(input("Enter a number: "))
    result = 10 / number
    print("Result:", result)
except ValueError:
    print("That's not a valid number!")
except ZeroDivisionError:
    print("You can't divide by zero!")
```

### Output (if the user enters `"0"`)

```plaintext
You can't divide by zero!
```

## Why Handle Errors?

Error handling ensures your program can:
1. **Handle Unexpected Inputs**: Provide meaningful feedback instead of crashing.
2. **Improve Reliability**: Continue running smoothly even when errors occur.
3. **Enhance User Experience**: Guide users on how to correct their mistakes.

## Summary

- Use `try` and `except` blocks to catch and handle errors gracefully.
- Specify different `except` blocks to handle multiple types of exceptions.
- Error handling ensures programs remain robust and user-friendly.

Mastering error handling is essential for building reliable and user-friendly programs. Practice with different types of errors to solidify your understanding.
