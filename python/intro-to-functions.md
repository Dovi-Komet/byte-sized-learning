---
layout: default
title: "Intro to Functions"
order: 17
---

Functions in Python are reusable blocks of code designed to perform specific tasks. They help make your programs more organized, modular, and easier to debug.

## What is a Function?

A function is defined using the `def` keyword, followed by a name, parentheses (which can include parameters), and a colon. The code inside the function is indented.

### Syntax:
```python
def function_name(parameters):
    # Code block
    return result
```

- `function_name`: The name of the function, which should follow naming conventions (lowercase with underscores).
- `parameters`: Optional inputs the function can accept.
- `return`: Optional keyword to send a value back to the caller.

## Defining and Calling a Function

To use a function, you first define it and then call it by its name.

### Example:
```python
def greet():
    print("Hello, World!")

# Calling the function
greet()
```

### Output:
```plaintext
Hello, World!
```

## Parameters in Functions

Functions can accept parameters to make them more flexible.

### Example:
```python
def greet_person(name):
    print(f"Hello, {name}!")

greet_person("Alice")
greet_person("Bob")
```

### Output:
```plaintext
Hello, Alice!
Hello, Bob!
```

## Returning Values

Functions can return values using the `return` statement.

### Example:
```python
def add(a, b):
    return a + b

result = add(5, 3)
print(f"The sum is {result}")
```

### Output:
```plaintext
The sum is 8
```

## Why Use Functions?

1. **Code Reusability**: Avoid repeating code by defining reusable functions.
2. **Improved Readability**: Functions help organize code into logical sections.
3. **Easier Maintenance**: Functions make debugging and updates simpler.

---

In the next lesson, we’ll dive deeper into return values and learn how to use them effectively.
