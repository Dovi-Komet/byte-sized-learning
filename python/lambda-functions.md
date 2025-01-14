---
layout: default
title: "Lambda Functions"
order: 48
---

Lambda functions in Python are anonymous functions defined using the `lambda` keyword. They are typically used for short, simple operations where defining a full function is unnecessary. Lambda functions can take any number of arguments but have only a single expression.

---

## Syntax of a Lambda Function

```python
lambda arguments: expression
```

- **`arguments`**: A comma-separated list of input parameters.
- **`expression`**: A single expression evaluated and returned.

### Example

```python
# A lambda function that adds 10 to its argument
add_ten = lambda x: x + 10
print(add_ten(5))  # Output: 15
```

---

## Key Differences Between Lambda and Regular Functions

1. **Syntax**: Lambda functions are defined in a single line, while regular functions use the `def` keyword.
2. **Name**: Lambda functions are anonymous unless assigned to a variable.
3. **Use Case**: Best for simple, short-lived operations.

---

## Using Lambda Functions with Built-in Functions

Lambda functions are often used with Python’s built-in functions like `map`, `filter`, and `sorted`.

### Example: Using `map`

The `map` function applies a lambda function to each item in an iterable.

```python
numbers = [1, 2, 3, 4]
squared = map(lambda x: x ** 2, numbers)
print(list(squared))  # Output: [1, 4, 9, 16]
```

---

### Example: Using `filter`

The `filter` function selects items from an iterable based on a condition.

```python
numbers = [1, 2, 3, 4, 5, 6]
even_numbers = filter(lambda x: x % 2 == 0, numbers)
print(list(even_numbers))  # Output: [2, 4, 6]
```

---

### Example: Using `sorted` with a Custom Key

The `sorted` function can use a lambda to define a custom sorting rule.

```python
names = ["Alice", "Bob", "Charlie"]
sorted_names = sorted(names, key=lambda name: len(name))
print(sorted_names)  # Output: ['Bob', 'Alice', 'Charlie']
```

---

## When to Use Lambda Functions

- When a short function is needed for immediate use.
- When you want to write concise code without defining a named function.
- Commonly in conjunction with functional programming tools like `map`, `filter`, and `sorted`.

---

## Limitations of Lambda Functions

1. **Single Expression**: They can only contain one expression and no statements.
2. **Readability**: Overuse can make code harder to read.
3. **Debugging**: Lack of a name makes debugging more difficult.

---

## Key Takeaways

- Lambda functions are useful for concise and functional-style programming.
- They should be used judiciously to maintain code readability.
- For complex operations, prefer defining regular functions with the `def` keyword.

---

In the next lesson, we’ll explore list comprehensions, a powerful feature for concise and efficient list manipulation in Python.
