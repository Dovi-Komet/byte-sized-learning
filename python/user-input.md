---
layout: default
title: "User Input"
order: 11
---

Python allows you to interact with users by collecting input from the keyboard using the `input()` function.

## The `input()` Function

The `input()` function displays a prompt (optional) and waits for the user to type something. When the user presses Enter, the input is returned as a string.

### Example:
```python
# Asking the user for their name
name = input("What is your name? ")
print(f"Hello, {name}!")
```

### Key Points:
- The argument of `input()` is the prompt displayed to the user.
- The return value is always a string, even if the user enters numbers.

## Converting Input

Since `input()` returns a string, you may need to convert it into another data type for calculations or comparisons.

### Example:
```python
# Asking the user for their age
age = input("How old are you? ")
age = int(age)  # Convert the string to an integer
print(f"Next year, you will be {age + 1} years old.")
```

### Common Conversions:
- `int(value)` converts to an integer.
- `float(value)` converts to a floating-point number.
- `bool(value)` converts to a boolean.

## Handling Errors

If the user enters something invalid for a conversion (e.g., typing "abc" when an integer is expected), Python will raise a `ValueError`. You can handle this using a `try-except` block.

### Example:
```python
try:
    number = int(input("Enter a number: "))
    print(f"You entered: {number}")
except ValueError:
    print("That’s not a valid number!")
```

## Practical Example

Here’s an example of a simple interactive program:

```python
# Collecting user details
name = input("What is your name? ")
age = input("How old are you? ")

# Displaying a personalized message
print(f"Nice to meet you, {name}. You are {age} years old.")
```

---

In the next lesson, we’ll explore boolean logic and how to make decisions in Python programs.
