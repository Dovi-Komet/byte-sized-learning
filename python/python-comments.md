---
layout: default
title: "Python Comments"
order: 6
---

Comments are lines in your code that Python ignores during execution. They are used to explain code, make it easier to read, or temporarily disable parts of the program.

## Single-Line Comments

In Python, a single-line comment starts with the `#` symbol. Everything after the `#` on that line is ignored by Python.

```python
# This is a single-line comment
print("Hello, World!")  # This prints a message to the screen
```

### Explanation
- The first line is a comment that explains the code.
- The comment after `print("Hello, World!")` describes what the line does.

## Multi-Line Comments (Using Multiple `#` Symbols)

Python doesn’t have a specific syntax for multi-line comments. However, you can use multiple single-line comments to achieve the same effect.

```python
# This is a multi-line comment
# Each line starts with a `#`
# Comments make code easier to understand
print("Python is fun!")
```

## Multi-Line Comments (Using Strings)

Alternatively, you can use triple-quoted strings (`"""` or `'''`) as multi-line comments. These are technically multi-line string literals but are often used as comments when not assigned to a variable.

```python
"""
This is a multi-line comment.
It spans multiple lines and is ignored by Python
when it’s not assigned to a variable.
"""
print("Learning Python!")
```

## Why Use Comments?

1. **Explain Code**: Make your code understandable for others (and yourself).
2. **Debugging**: Temporarily disable parts of your code by commenting them out.
3. **Documentation**: Provide details about what specific blocks of code do.

---

In the next lesson, we’ll explore variables and types in Python.
