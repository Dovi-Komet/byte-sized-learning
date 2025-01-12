---
layout: default
title: "Formatted Strings"
order: 16
---

Formatted strings in Python allow you to embed variables and expressions directly within string text, making it easier to create dynamic content. Python provides multiple ways to format strings, including f-strings, `str.format()`, and the `%` operator.

## f-Strings (Recommended)

Introduced in Python 3.6, f-strings are the most modern and efficient way to format strings. They use the `f` prefix and curly braces `{}` to embed variables or expressions directly.

### Syntax:
```python
f"Your text here {variable_or_expression}"
```

### Example:
```python
name = "Alice"
age = 30

print(f"My name is {name} and I am {age} years old.")
```

### Output:
```plaintext
My name is Alice and I am 30 years old.
```

### Inline Expressions:
You can include expressions inside f-strings.

```python
x = 5
y = 10

print(f"The sum of {x} and {y} is {x + y}.")
```

### Output:
```plaintext
The sum of 5 and 10 is 15.
```

## `str.format()`

The `str.format()` method was the primary way to format strings before f-strings.

### Example:
```python
name = "Bob"
age = 25

print("My name is {} and I am {} years old.".format(name, age))
```

### Output:
```plaintext
My name is Bob and I am 25 years old.
```

### Using Positional and Keyword Arguments:
```python
print("Name: {0}, Age: {1}".format("Carol", 40))
print("Name: {name}, Age: {age}".format(name="Dave", age=35))
```

### Output:
```plaintext
Name: Carol, Age: 40
Name: Dave, Age: 35
```

## Using the `%` Operator (Old Style)

The `%` operator is an older way to format strings. While still supported, it’s generally not recommended for new code.

### Example:
```python
name = "Eve"
age = 28

print("My name is %s and I am %d years old." % (name, age))
```

### Output:
```plaintext
My name is Eve and I am 28 years old.
```

## Formatting Numbers

You can format numbers to control their precision, width, or alignment.

### Example (f-strings):
```python
pi = 3.14159265

print(f"Pi rounded to 2 decimal places: {pi:.2f}")
print(f"Pi padded to 10 characters: {pi:10.2f}")
```

### Output:
```plaintext
Pi rounded to 2 decimal places: 3.14
Pi padded to 10 characters:       3.14
```

## Choosing a Formatting Method

- Use **f-strings** for new code due to their readability and efficiency.
- Use `str.format()` for compatibility with older versions of Python (before 3.6).
- Avoid the `%` operator for modern Python code.

---

In the next lesson, we’ll introduce the concept of functions and how to create reusable blocks of code.
