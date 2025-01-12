---
layout: default
title: "print Function"
order: 5
---

## The `print()` Function

The `print()` function is one of the most commonly used functions in Python. It allows you to display information on the screen, which is essential for interacting with your program.

### Syntax of the `print()` Function

The basic syntax of the `print()` function is:

```python
print(<message>)
```

- `<message>`: The information you want to display. This can be text, numbers, or other types of data.

### Printing Text

To print text, enclose the message in double (`"`) or single (`'`) quotes:

```python
print("Hello, Python!")
print('Welcome to the print() function.')
```

#### Output:
```plaintext
Hello, Python!
Welcome to the print() function.
```

### Printing Numbers

You can also print numbers directly without using quotes:

```python
print(42)
print(3.14)
```

#### Output:
```plaintext
42
3.14
```

### Combining Text and Variables

You can use the `print()` function to display both text and variable values:

```python
name = "Alice"
age = 30
print("Name:", name)
print("Age:", age)
```

#### Output:
```plaintext
Name: Alice
Age: 30
```

### Using `print()` for Debugging

The `print()` function is often used to debug programs by checking the values of variables or the flow of execution.

---

In the next lesson, we’ll learn about comments and how to use them effectively in Python.
