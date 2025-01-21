---
title: "Conditionals"
order: 12
---

# Conditionals

Conditionals allow your program to make decisions based on certain conditions. They enable you to execute specific blocks of code depending on whether a condition evaluates to `True` or `False`.

---

## The `if` Statement

The `if` statement is the simplest conditional. If the condition evaluates to `True`, the code block inside it runs.

### Syntax:
```python
if condition:
    # Code to execute if condition is True
```

### Example:
```python
age = 18

if age >= 18:
    print("You are eligible to vote.")
```

---

## The `if-else` Statement

Use `if-else` to specify an alternative block of code to run if the condition is `False`.

### Syntax:
```python
if condition:
    # Code to execute if condition is True
else:
    # Code to execute if condition is False
```

### Example:
```python
age = 16

if age >= 18:
    print("You are eligible to vote.")
else:
    print("You are not eligible to vote.")
```

---

## The `if-elif-else` Statement

When you have multiple conditions, use `elif` (short for "else if"). The `else` block is optional and executes if none of the conditions are `True`.

### Syntax:
```python
if condition1:
    # Code for condition1
elif condition2:
    # Code for condition2
else:
    # Code if no conditions are True
```

### Example:
```python
grade = 85

if grade >= 90:
    print("Grade: A")
elif grade >= 80:
    print("Grade: B")
elif grade >= 70:
    print("Grade: C")
else:
    print("Grade: F")
```

---

## Nested Conditionals

Conditionals can be nested inside other conditionals for more complex logic.

### Example:
```python
age = 20
citizen = True

if age >= 18:
    if citizen:
        print("You are eligible to vote.")
    else:
        print("You must be a citizen to vote.")
else:
    print("You are not old enough to vote.")
```

---

## Conditional Expressions (Ternary Operator)

Python supports a shorthand way of writing conditionals using a single line.

### Syntax:
```python
value = true_value if condition else false_value
```

### Example:
```python
age = 18
status = "Adult" if age >= 18 else "Minor"
print(status)  # Adult
```

---

## Common Pitfalls

1. **Indentation Errors**: Always use consistent indentation for the code blocks inside conditionals.
   ```python
   if True:
   print("This will cause an error!")  # IndentationError
   ```

2. **Logical Mistakes**: Ensure your conditions are logically correct to avoid unexpected results.

---

## Practice Exercises

1. Write a program that:
   - Asks the user for a number.
   - Prints whether the number is even or odd.

2. Create a program to:
   - Ask the user for their age.
   - Print one of the following:
     - "Child" if age < 13.
     - "Teenager" if 13 ≤ age < 20.
     - "Adult" if age ≥ 20.

3. Build a simple calculator:
   - Ask the user for two numbers and an operation (`+`, `-`, `*`, `/`).
   - Perform the operation and print the result. Handle invalid operators gracefully.

Conditionals are a powerful tool for making your programs dynamic and responsive to user input!
