---
layout: default
title: "Loops: The `for` Loop"
order: 13
---

A `for` loop is used to iterate over a sequence (like a list, string, or range of numbers).

### Basic `for` Loop

Example:

```python
for number in range(5):
    print("Number is:", number)
```

### Expected Output

```plaintext
Number is: 0
Number is: 1
Number is: 2
Number is: 3
Number is: 4
```

### Looping Through a List

Example:

```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print("I like", fruit)
```

### Expected Output

```plaintext
I like apple
I like banana
I like cherry
```

### Looping Through a String

Example:

```python
word = "Python"
for letter in word:
    print(letter)
```

### Expected Output

```plaintext
P
y
t
h
o
n
```

The `for` loop is a versatile tool for working with sequences.