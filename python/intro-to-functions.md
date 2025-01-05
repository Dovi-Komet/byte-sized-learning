---
layout: default
title: "Intro to Functions"
order: 16
---

Functions are reusable blocks of code designed to perform specific tasks. They help make your code more organized, readable, and efficient by avoiding repetition.

## Defining a Function

In Python, you define a function using the `def` keyword, followed by the function name and parentheses `()`.

### Example: Defining a Function

```python
def greet():
    print("Hello!")
```

This creates a function named `greet` that prints "Hello!" when called.

## Calling a Function

To execute a function, you call it by its name followed by parentheses.

### Example: Calling a Function

```python
greet()
```

### Expected Output

```plaintext
Hello!
```

## Functions with Parameters

Parameters allow you to pass information to a function so it can operate on different values.

### Example: Function with Parameters

```python
def greet(name):
    print("Hello, " + name + "!")
greet("Alice")
```

### Expected Output

```plaintext
Hello, Alice!
```

In this example:
- The `name` parameter is a placeholder for the value you pass when calling the function.
- `"Alice"` is passed to the `greet` function, and the function uses it to generate a personalized message.

## Summary

- Functions help organize and reuse code efficiently.
- Define a function with `def`, followed by a name and parentheses.
- Call a function by its name followed by parentheses.
- Use parameters to pass information into functions for flexibility.

Functions are a powerful tool in Python, and this is just the beginning. In the next lesson, we’ll learn how to return values from functions to make them even more versatile.
