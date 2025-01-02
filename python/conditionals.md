---
layout: default
title: "Conditionals"
order: 13
---

Conditional statements allow your program to make decisions based on certain conditions. Python uses `if`, `elif`, and `else` for this.

### Basic `if` Statement

The `if` statement runs a block of code if a condition is true.

Example:

```python
age = 18
if age >= 18:
    print("You are an adult.")
```

### Expected Output

```plaintext
You are an adult.
```

### Adding `else`

The `else` statement runs a block of code when the condition in the `if` statement is false.

Example:

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

### Using `elif`

The `elif` (short for "else if") statement lets you check multiple conditions.

Example:

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