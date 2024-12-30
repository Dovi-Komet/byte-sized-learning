---
layout: default
title: "Functions: Return Values"
order: 15
---

Functions can return values that you can use later in your program.

### Using the `return` Statement

Example:

```python
def add(a, b):
    return a + b

result = add(5, 3)
print("The result is:", result)
```

### Expected Output

```plaintext
The result is: 8
```

### Why Use Return Values?

Returning values makes functions more flexible and allows you to store the results for further use.

Example:

```python
def square(number):
    return number * number

x = square(4)
y = square(5)
print("Squares:", x, y)
```

### Expected Output

```plaintext
Squares: 16 25
```