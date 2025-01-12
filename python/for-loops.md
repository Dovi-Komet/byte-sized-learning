---
layout: default
title: "for Loops"
order: 15
---

A `for` loop in Python is used to iterate over a sequence (like a list, tuple, string, or range). It allows you to execute a block of code for each item in the sequence.

## Syntax of `for` Loop
```python
for item in sequence:
    # Code to execute for each item
```

### Example:
```python
fruits = ["apple", "banana", "cherry"]

for fruit in fruits:
    print(f"I like {fruit}")
```

### Output:
```plaintext
I like apple
I like banana
I like cherry
```

## Iterating Over a Range

The `range()` function generates a sequence of numbers, which is commonly used with `for` loops.

### Example:
```python
for num in range(5):
    print(f"Number: {num}")
```

### Output:
```plaintext
Number: 0
Number: 1
Number: 2
Number: 3
Number: 4
```

### Custom Range
You can specify a start, stop, and step for the `range()` function.

```python
for num in range(1, 10, 2):
    print(num)
```

### Output:
```plaintext
1
3
5
7
9
```

## Iterating Over Strings

You can use a `for` loop to iterate through each character in a string.

### Example:
```python
for char in "Python":
    print(char)
```

### Output:
```plaintext
P
y
t
h
o
n
```

## Using `break` in `for` Loops

The `break` statement stops the loop before it completes all iterations.

### Example:
```python
for num in range(10):
    if num == 5:
        break
    print(num)
```

### Output:
```plaintext
0
1
2
3
4
```

## Using `continue` in `for` Loops

The `continue` statement skips the current iteration and moves to the next one.

### Example:
```python
for num in range(5):
    if num == 2:
        continue
    print(num)
```

### Output:
```plaintext
0
1
3
4
```

## Using `else` with `for`

The `else` block runs after the `for` loop completes, but it is skipped if the loop is terminated with a `break`.

### Example:
```python
for num in range(5):
    print(num)
else:
    print("Loop completed!")
```

### Output:
```plaintext
0
1
2
3
4
Loop completed!
```

---

In the next lesson, we’ll explore how to format strings in Python using f-strings and other methods.
