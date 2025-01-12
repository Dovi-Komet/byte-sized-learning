---
layout: default
title: "Return Values"
order: 18
---

Functions in Python can send data back to the part of the program that called them using the `return` statement. This allows you to reuse the output of a function for further processing.

## The `return` Statement

The `return` statement ends a function and sends a value back to the caller. Without a `return` statement, a function returns `None` by default.

### Syntax:
```python
def function_name(parameters):
    # Code block
    return value
```

## Returning a Single Value

A function can return a single value for use in the rest of the program.

### Example:
```python
def square(number):
    return number ** 2

result = square(4)
print(f"The square of 4 is {result}")
```

### Output:
```plaintext
The square of 4 is 16
```

## Returning Multiple Values

A function can return multiple values using a tuple.

### Example:
```python
def calculate(a, b):
    sum = a + b
    difference = a - b
    return sum, difference

result_sum, result_difference = calculate(10, 5)
print(f"Sum: {result_sum}, Difference: {result_difference}")
```

### Output:
```plaintext
Sum: 15, Difference: 5
```

## Using Return Values in Expressions

The returned value can be used directly in other operations or expressions.

### Example:
```python
def multiply(a, b):
    return a * b

print(f"Product: {multiply(3, 7)}")
print(f"Double the product: {multiply(3, 7) * 2}")
```

### Output:
```plaintext
Product: 21
Double the product: 42
```

## Why Use Return Values?

1. **Reusability**: Functions with return values can be used in various parts of the program.
2. **Flexibility**: Returning values allows for complex operations and further computations.
3. **Modularity**: Simplifies code by separating logic into reusable components.

---

In the next lesson, we’ll explore Python’s list data structure and how to work with collections of data.
