---
layout: default
title: "while Loops"
order: 14
---

A `while` loop allows you to repeat a block of code as long as a condition evaluates to `True`. This makes it useful for situations where the number of iterations isn’t fixed and depends on a condition.

## Basic `while` Loop

The basic syntax for a `while` loop is:

```python
while condition:
    # Code to execute repeatedly
```

The loop will run as long as the condition is `True`. Be sure to update variables inside the loop to eventually make the condition `False`, or the loop may never end.

### Example: Counting with a `while` Loop

```python
count = 0
while count < 5:
    print("Count is:", count)
    count += 1  # Increment count
```

### Expected Output

```plaintext
Count is: 0
Count is: 1
Count is: 2
Count is: 3
Count is: 4
```

## Understanding the Increment Operator (`+=`)

The increment operator `+=` is a shorthand way to increase the value of a variable. It combines addition with assignment, updating the variable in place.

### Example: Using `+=`

```python
count = 0
count += 1  # Equivalent to count = count + 1
print(count)  # 1
```

The same concept applies to other operators like `-=`, `*=`, and `/=` for subtraction, multiplication, and division, respectively.

## Infinite Loops

If the condition in a `while` loop never becomes `False`, the loop will run indefinitely, creating an infinite loop. Use `Ctrl + C` in the terminal to stop it.

### Example: Infinite Loop

```python
while True:
    print("This will run forever!")
```

While infinite loops can be problematic, they are sometimes intentionally used in programs with specific exit conditions.

## Breaking Out of a Loop

The `break` statement allows you to exit a loop before the condition becomes `False`.

### Example: Breaking a Loop

```python
count = 0
while True:
    print("Count is:", count)
    count += 1
    if count == 5:
        break  # Exit the loop when count reaches 5
```

### Expected Output

```plaintext
Count is: 0
Count is: 1
Count is: 2
Count is: 3
Count is: 4
```

## Avoiding Common Pitfalls

1. **Unintended Infinite Loops**: Always ensure your loop condition can become `False`.
   ```python
   count = 0
   while count < 5:  # Correctly set a condition
       print("Count is:", count)
       count += 1
   ```

2. **Misplaced `break` Statements**: Make sure `break` is used inside the loop, usually within a condition.
   ```python
   while True:
       if some_condition:
           break  # Exit the loop safely
   ```

## Summary

- Use `while` loops to repeat code while a condition is `True`.
- Increment operators like `+=` make it easy to update variables within a loop.
- Avoid infinite loops unless intentional, and use `Ctrl + C` to stop them in the terminal.
- Use `break` to exit a loop early if necessary.
- Always update variables within the loop to ensure the condition eventually becomes `False`.

Practice writing `while` loops and using increment operators to handle dynamic, condition-based repetition in your programs!
