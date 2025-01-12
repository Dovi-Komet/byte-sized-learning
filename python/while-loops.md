---
layout: default
title: "while Loops"
order: 14
---

Loops allow you to repeat a block of code as long as a condition is true. The `while` loop is one of Python’s looping constructs.

## The `while` Loop

The `while` loop keeps executing as long as its condition evaluates to `True`.

### Syntax:
```python
while condition:
    # Code to execute repeatedly
```

### Example:
```python
count = 0

while count < 5:
    print(f"Count is {count}")
    count += 1  # Increment count to avoid an infinite loop
```

### Explanation:
1. The `while` loop starts by checking the condition `count < 5`.
2. If the condition is `True`, the code inside the loop runs.
3. The loop increments `count` on each iteration.
4. When `count` becomes `5`, the condition evaluates to `False`, and the loop stops.

## Infinite Loops

If the condition in a `while` loop never becomes `False`, the loop runs indefinitely. Be cautious to avoid infinite loops in your code.

### Example of an Infinite Loop:
```python
while True:
    print("This will run forever!")
```

You can stop an infinite loop manually by pressing `Ctrl + C` in the terminal.

## The `break` Statement

The `break` statement lets you exit a loop prematurely, even if the condition is still `True`.

### Example:
```python
count = 0

while True:
    print(f"Count is {count}")
    count += 1
    if count == 5:  # Exit the loop when count reaches 5
        break
```

## The `continue` Statement

The `continue` statement skips the rest of the current loop iteration and moves to the next one.

### Example:
```python
count = 0

while count < 5:
    count += 1
    if count == 3:  # Skip when count is 3
        continue
    print(f"Count is {count}")
```

### Output:
```plaintext
Count is 1
Count is 2
Count is 4
Count is 5
```

## Using `else` with `while`

You can use an `else` block with a `while` loop. The `else` block runs only if the loop wasn’t terminated by a `break` statement.

### Example:
```python
count = 0

while count < 3:
    print(f"Count is {count}")
    count += 1
else:
    print("Loop completed successfully.")
```

---

In the next lesson, we’ll explore the `for` loop and how it can be used to iterate over sequences.
