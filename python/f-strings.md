---
title: "f-Strings"
order: 9
---

# f-Strings

Python’s **f-strings** (formatted string literals) provide a concise and efficient way to embed expressions and variables into strings. Introduced in Python 3.6, f-strings make string formatting easier and more readable.

## Creating an f-String

To create an f-string:
1. Start the string with an `f` or `F`.
2. Use curly braces `{}` to include expressions or variables.

### Example:
```python
name = "Alice"
age = 30

# f-string with variables
message = f"My name is {name} and I am {age} years old."
print(message)  # My name is Alice and I am 30 years old.
```

---

## Embedding Expressions

f-Strings can evaluate expressions directly within curly braces.

### Example:
```python
a = 5
b = 3

print(f"{a} + {b} = {a + b}")  # 5 + 3 = 8
print(f"The square of {a} is {a**2}.")  # The square of 5 is 25.
```

---

## Formatting Numbers

f-Strings support number formatting for enhanced output:

| Format Specifier   | Description                                | Example                  | Result       |
|--------------------|--------------------------------------------|--------------------------|--------------|
| `.nf`             | Round to `n` decimal places               | `f"{3.14159:.2f}"`      | `3.14`       |
| `,`               | Adds a comma as a thousands separator      | `f"{1000000:,}"`        | `1,000,000`  |
| `e`               | Scientific notation                       | `f"{1234:e}"`           | `1.234000e+03` |
| `%`               | Percentage                                | `f"{0.75:.0%}"`         | `75%`        |

### Examples:
```python
value = 12345.6789

# Round to 2 decimal places
print(f"Value: {value:.2f}")  # Value: 12345.68

# Add commas
print(f"Formatted: {value:,.2f}")  # Formatted: 12,345.68

# Percentage
percentage = 0.85
print(f"Success Rate: {percentage:.1%}")  # Success Rate: 85.0%
```

---

## Multiline f-Strings

Use triple quotes for multiline f-strings:
```python
name = "Alice"
age = 30

message = f"""
Name: {name}
Age: {age}
Status: {"Adult" if age >= 18 else "Minor"}
"""
print(message)
```

---

## Using f-Strings with Functions

You can call functions directly within f-strings:
```python
def greet(name):
    return f"Hello, {name}!"

print(f"{greet('Alice')} Welcome to Python.")  # Hello, Alice! Welcome to Python.
```

---

## Escaping Braces in f-Strings
{%raw%}
To include literal curly braces `{` or `}` in an f-string, double them:
```python
print(f"{{}} is an empty set of braces.")  # {} is an empty set of braces.
```
{% endraw %}
---

## Practice Exercises

1. Create variables for:
   - Your name.
   - Your favorite color.
   - Your favorite number.
   Use an f-string to print a sentence including all three variables.

2. Calculate and display the following using f-strings:
   - The area of a circle with a radius of `7` (use `3.14` for π).
   - A salary increase of `15%` for an initial salary of `$50,000`.

3. Print a formatted table:
   - Product names and their prices.
   - Align product names to the left and prices to the right, formatted to two decimal places.

f-Strings are a powerful and convenient feature for dynamic string formatting in Python. They make your code cleaner and easier to read!