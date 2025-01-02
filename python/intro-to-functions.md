---
layout: default
title: "Intro to Functions"
order: 16
---

Functions are reusable blocks of code that perform specific tasks. They help make your code more organized and efficient.

### Defining a Function

Use the `def` keyword to define a function.

Example:

```python
def greet():
    print("Hello!")
```

### Calling a Function

To use a function, you call it by its name followed by parentheses.

Example:

```python
greet()
```

### Expected Output

```plaintext
Hello!
```

### Functions with Parameters

You can pass information to a function using parameters.

Example:

```python
def greet(name):
    print("Hello, " + name + "!")
greet("Alice")
```

### Expected Output

```plaintext
Hello, Alice!
```