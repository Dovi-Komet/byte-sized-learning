---
layout: default
title: "Conditionals"
order: 13
---

Conditional statements allow your program to make decisions based on certain conditions. Python uses `if`, `elif`, and `else` for this purpose.

## The Role of Booleans in Conditionals

Conditionals in Python rely on Boolean expressions to determine whether a block of code should execute. A Boolean expression evaluates to either `True` or `False`.

For example, consider the expression `age >= 18`. This evaluates to `True` if `age` is 18 or greater; otherwise, it evaluates to `False`. The result of the expression determines which block of code runs.

## Basic `if` Statement

The `if` statement runs a block of code only if the condition evaluates to `True`.

### Example: `if` Statement

```python
age = 18
if age >= 18:
    print("You are an adult.")
```

### Expected Output

```plaintext
You are an adult.
```

## Adding `else`

The `else` statement provides an alternative block of code to run when the condition in the `if` statement is `False`.

### Example: `if` with `else`

```python
age = 16
if age >= 18:
    print("You are an adult.")
else:
    print("You are a minor.")
```

### Expected Output

```plaintext
You are a minor.
```

## Using `elif`

The `elif` (short for "else if") statement allows you to check additional conditions. Python evaluates conditions in order, and the first one that evaluates to `True` runs.

### Example: `if`, `elif`, and `else`

```python
age = 20
if age < 13:
    print("You are a child.")
elif age < 18:
    print("You are a teenager.")
else:
    print("You are an adult.")
```

### Expected Output

```plaintext
You are an adult.
```

## Indentation Matters

In Python, indentation defines the blocks of code that belong to `if`, `elif`, or `else`. Improper indentation will result in an error.

### Example: Indentation Error

```python
age = 18
if age >= 18:
print("You are an adult.")  # This line is not indented correctly
```

### Error Output

```plaintext
IndentationError: expected an indented block
```

## Summary

- Boolean expressions evaluate to `True` or `False` and determine which code block runs.
- Use `if` for a single condition, `else` for an alternative case, and `elif` to check additional conditions.
- Proper indentation is essential in Python for conditionals to work correctly.

Practice creating conditions with `if`, `elif`, and `else` to make your programs dynamic and responsive!
