---
layout: default
title: "Return Values"
order: 18
---

Functions can return values that you can use later in your program. The `return` statement allows a function to send a result back to the caller.

## Using the `return` Statement

The `return` statement specifies the value a function should send back to where it was called. 

### Example: Returning a Value

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

Here:
- The `add` function computes the sum of `a` and `b`.
- The `return` statement sends the result (`8`) back to the variable `result`.

## Why Use Return Values?

Returning values makes functions more versatile and allows you to store and reuse the results in different parts of your program.

### Example: Reusing Returned Values

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

In this example:
- The `square` function calculates the square of a number and returns the result.
- The returned values are stored in `x` and `y`, which are then printed.

## Using Returned Values in Expressions

You can use returned values directly in expressions or other functions.

### Example: Using Returned Values

```python
def multiply(a, b):
    return a * b

def add_and_multiply(x, y, z):
    sum_result = x + y
    return multiply(sum_result, z)

result = add_and_multiply(2, 3, 4)
print("Result:", result)
```

### Expected Output

```plaintext
Result: 20
```

In this example:
- The `add_and_multiply` function adds two numbers, then multiplies the result with a third number using the `multiply` function.

## Summary

- Use the `return` statement to send a result back to the caller.
- Returning values allows you to store and reuse the results for further calculations or operations.
- Functions can return values that are directly used in expressions or passed to other functions.

Mastering return values will help you build more dynamic and modular programs. Practice writing functions that return and use values to enhance your coding skills!
