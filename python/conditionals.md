---
layout: default
title: "Conditionals"
order: 13
---

Conditionals allow your Python programs to make decisions based on certain conditions. They let you control the flow of your program using boolean logic.

## The `if` Statement

The `if` statement executes a block of code only if a condition evaluates to `True`.

### Syntax:
```python
if condition:
    # Code to execute if condition is True
```

### Example:
```python
age = 18

if age >= 18:
    print("You are an adult.")
```

## The `else` Statement

The `else` statement provides a block of code to execute when the condition in the `if` statement is `False`.

### Example:
```python
age = 16

if age >= 18:
    print("You are an adult.")
else:
    print("You are a minor.")
```

## The `elif` Statement

The `elif` (short for "else if") statement checks additional conditions when the initial `if` condition is `False`. You can use multiple `elif` statements.

### Example:
```python
age = 20

if age < 13:
    print("You are a child.")
elif age < 18:
    print("You are a teenager.")
else:
    print("You are an adult.")
```

## Nested Conditionals

Conditionals can be nested within each other to check multiple levels of conditions.

### Example:
```python
age = 20
has_id = True

if age >= 18:
    if has_id:
        print("You can enter.")
    else:
        print("You need an ID to enter.")
else:
    print("You are not old enough to enter.")
```

## Logical Operators with Conditionals

You can combine multiple conditions using logical operators like `and`, `or`, and `not`.

### Example:
```python
age = 20
has_ticket = True

if age >= 18 and has_ticket:
    print("You can watch the movie.")
else:
    print("You cannot watch the movie.")
```

---

In the next lesson, we’ll learn how to use loops to repeat actions in Python.
