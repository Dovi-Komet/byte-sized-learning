---
layout: default
title: "Formatted Strings"
order: 15.5
---

Formatted strings, also known as f-strings, are a powerful feature in Python that allow you to create strings with embedded expressions. This makes it easy to dynamically include values in your text.

## What Are Formatted Strings?

Formatted strings are strings prefixed with the letter `f` or `F`. You can include expressions inside curly braces `{}` within the string, and Python will evaluate and insert their values.

### Example: Basic Formatted String

```python
name = "Alice"
age = 30
print(f"My name is {name} and I am {age} years old.")
```

### Output:

```plaintext
My name is Alice and I am 30 years old.
```

## Using Expressions in Formatted Strings

You can include any valid Python expression inside curly braces.

### Example: Calculations and Methods

```python
num1 = 10
num2 = 5
print(f"The sum of {num1} and {num2} is {num1 + num2}.")
print(f"My name in uppercase is {name.upper()}.")
```

### Output:

```plaintext
The sum of 10 and 5 is 15.
My name in uppercase is ALICE.
```

## Formatting Numbers

You can format numbers for better readability, such as specifying decimal places or adding commas.

### Example: Formatting Numbers

```python
pi = 3.141592653589793
large_number = 1234567890

print(f"Pi rounded to 2 decimal places: {pi:.2f}")
print(f"Large number with commas: {large_number:,}")
```

### Output:

```plaintext
Pi rounded to 2 decimal places: 3.14
Large number with commas: 1,234,567,890
```

## Combining Formatted Strings with Loops

Formatted strings can be very useful when working with loops.

### Example: Using Formatted Strings in a Loop

```python
for i in range(1, 4):
    print(f"Iteration {i}: {i**2} squared is {i**2}.")
```

### Output:

```plaintext
Iteration 1: 1 squared is 1.
Iteration 2: 4 squared is 4.
Iteration 3: 9 squared is 9.
```

## Summary

- Formatted strings (f-strings) allow you to include expressions directly within strings.
- Use curly braces `{}` to embed variables, expressions, or method calls.
- Format numbers with options like `:.2f` for decimal places or `:,` for commas.
- f-strings simplify dynamic string creation and make your code more readable.

Practice using formatted strings to create dynamic and flexible outputs in your Python programs!
