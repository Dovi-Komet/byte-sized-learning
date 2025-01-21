---
title: "Loops"
order: 13
---

# Loops

**Loops** allow you to execute a block of code multiple times. Python provides two main types of loops: `for` loops and `while` loops.

---

## `for` Loops

A `for` loop iterates over a sequence (like a list, tuple, or string) and executes the code block for each item.

### Syntax:
```python
for item in sequence:
    # Code to execute for each item
```

### Example:
```python
# Iterating through a list
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)

# Iterating through a string
for letter in "Python":
    print(letter)
```

### Using `range()`:
The `range()` function generates a sequence of numbers.
```python
# From 0 to 4
for i in range(5):
    print(i)

# From 1 to 5
for i in range(1, 6):
    print(i)

# With a step
for i in range(0, 10, 2):
    print(i)
```

---

## `while` Loops

A `while` loop continues to execute as long as its condition is `True`.

### Syntax:
```python
while condition:
    # Code to execute while condition is True
```

### Example:
```python
count = 0
while count < 5:
    print(count)
    count += 1
```

---

## Controlling Loops

### `break` Statement:
Stops the loop immediately.
```python
for i in range(10):
    if i == 5:
        break
    print(i)
```

### `continue` Statement:
Skips the rest of the current iteration and moves to the next.
```python
for i in range(10):
    if i % 2 == 0:
        continue
    print(i)  # Prints odd numbers
```

### `else` Clause with Loops:
Executes after the loop finishes, unless the loop is terminated with `break`.
```python
for i in range(5):
    print(i)
else:
    print("Loop completed!")
```

---

## Nested Loops

You can place a loop inside another loop.

### Example:
```python
for i in range(3):
    for j in range(2):
        print(f"i: {i}, j: {j}")
```

---

## Infinite Loops

A loop runs forever if its condition never becomes `False`. Use with caution and always include a way to exit.
```python
while True:
    user_input = input("Type 'exit' to quit: ")
    if user_input.lower() == "exit":
        break
```

---

## Common Use Cases

1. **Iterating Over a List**:
   ```python
   numbers = [1, 2, 3, 4, 5]
   for num in numbers:
       print(num)
   ```

2. **Counting Down**:
   ```python
   countdown = 5
   while countdown > 0:
       print(countdown)
       countdown -= 1
   print("Blastoff!")
   ```

3. **Finding Factors of a Number**:
   ```python
   number = int(input("Enter a number: "))
   for i in range(1, number + 1):
       if number % i == 0:
           print(i)
   ```

---

## Practice Exercises

1. Write a program to:
   - Print all numbers from 1 to 20.
   - Skip numbers divisible by 3.

2. Create a program that:
   - Asks the user to guess a secret number.
   - Keep asking until they guess correctly.

3. Generate a multiplication table (from 1 to 10) for a number entered by the user.

Loops are essential for automating repetitive tasks and are a key part of programming in Python!
