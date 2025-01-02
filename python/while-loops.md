---
layout: default
title: "while Loops"
order: 14
---

A `while` loop allows you to repeat a block of code as long as a condition is true.

### Basic `while` Loop

Example:

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

### Infinite Loops

Be careful! If the condition in a `while` loop never becomes false, the loop will run forever. To stop an infinite loop, use `Ctrl + C` in the terminal.

Example:

```python
while True:
    print("This will run forever!")
```

### Breaking Out of a Loop

Use the `break` statement to exit a loop early.

Example:

```python
count = 0
while True:
    print("Count is:", count)
    count += 1
    if count == 5:
        break  # Exit the loop when count is 5
```

### Expected Output

```plaintext
Count is: 0
Count is: 1
Count is: 2
Count is: 3
Count is: 4
```