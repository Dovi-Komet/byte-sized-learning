---
title: "Lambda Functions"
order: 15
---

# Lambda Functions

**Lambda functions**, also known as anonymous functions, are small, one-line functions defined without a name. They are often used for short, simple operations where defining a full function would be unnecessary.

---

## Syntax

### General Syntax:
```python
lambda arguments: expression
```

- **`lambda`**: The keyword used to define a lambda function.
- **`arguments`**: Inputs to the function (like parameters in regular functions).
- **`expression`**: The single operation or computation the function performs.

---

## Example

Here’s a simple example:
```python
# Lambda function to add two numbers
add = lambda x, y: x + y
print(add(3, 5))  # Output: 8
```

---

## Differences from Regular Functions

1. **No Name**: Lambda functions are anonymous.
2. **One Expression**: A lambda function can only contain a single expression. It automatically returns the result of this expression.
3. **Compact**: Useful for short, simple operations.

### Regular Function vs Lambda Function:
```python
# Regular function
def square(x):
    return x * x

# Lambda function
square = lambda x: x * x

print(square(4))  # Output: 16
```

---

## Using Lambda Functions

### With `map()`
The `map()` function applies a lambda function to all items in an iterable (e.g., list).
```python
numbers = [1, 2, 3, 4]
squared = map(lambda x: x * x, numbers)
print(list(squared))  # Output: [1, 4, 9, 16]
```

### With `filter()`
The `filter()` function uses a lambda to determine which items to keep from an iterable.
```python
numbers = [1, 2, 3, 4, 5, 6]
even_numbers = filter(lambda x: x % 2 == 0, numbers)
print(list(even_numbers))  # Output: [2, 4, 6]
```

### With `sorted()`
The `sorted()` function can use a lambda to define a custom sort key.
```python
names = ["Alice", "Bob", "Charlie"]
sorted_names = sorted(names, key=lambda x: len(x))
print(sorted_names)  # Output: ['Bob', 'Alice', 'Charlie']
```

---

## Nested Lambda Functions

You can use a lambda function as a parameter or even return it from another function.

### Example:
```python
def multiplier(n):
    return lambda x: x * n

double = multiplier(2)
triple = multiplier(3)

print(double(5))  # Output: 10
print(triple(5))  # Output: 15
```

---

## Limitations of Lambda Functions

1. **Single Expression**: Lambdas can only execute a single expression. For complex logic, use a regular function.
2. **Readability**: Overusing lambdas can make code harder to understand.

---

## Best Practices

- Use lambda functions for **simple operations**.
- Avoid using lambdas for **complex logic** or when readability is a concern.

---

## Practice Exercises

1. Use a lambda function with `map()` to:
   - Double all numbers in a list: `[1, 2, 3, 4]`.

2. Use a lambda function with `filter()` to:
   - Extract all words longer than 4 characters from a list: `["apple", "cat", "banana", "dog"]`.

3. Create a function `power(n)` that:
   - Returns a lambda function to calculate the `n`th power of a number.
   - Example: `power(2)(3)` should return `9`.

Lambda functions are a powerful tool for writing concise and functional-style Python code!