---
layout: default
title: "for Loops"
order: 15
---

A `for` loop is used to iterate over a sequence (like a list, string, or range of numbers). It allows you to execute a block of code once for each item in the sequence.

## Basic `for` Loop

The `for` loop iterates over a sequence, assigning each item to a variable in turn.

### Example: Iterating Over a Range

```python
for number in range(5):
    print("Number is:", number)
```

The `range(5)` function generates numbers from `0` to `4` (not including `5`).

### Expected Output

```plaintext
Number is: 0
Number is: 1
Number is: 2
Number is: 3
Number is: 4
```

## Looping Through a List

You can use a `for` loop to iterate over items in a list.

### Example: Iterating Over a List

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

## Looping Through a String

Strings are sequences of characters, so you can iterate over them with a `for` loop.

### Example: Iterating Over a String

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

## Using `break` in a `for` Loop

You can use the `break` statement to exit a `for` loop early.

### Example: Breaking a Loop

```python
for number in range(10):
    if number == 5:
        break  # Exit the loop when number is 5
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

## Using `continue` in a `for` Loop

The `continue` statement skips the current iteration and moves to the next.

### Example: Skipping Iterations

```python
for number in range(5):
    if number == 2:
        continue  # Skip when number is 2
    print("Number is:", number)
```

### Expected Output

```plaintext
Number is: 0
Number is: 1
Number is: 3
Number is: 4
```

## Summary

- Use `for` loops to iterate over sequences like lists, strings, or ranges.
- The `range()` function generates a sequence of numbers.
- Use `break` to exit a loop early and `continue` to skip to the next iteration.
- Practice combining `for` loops with sequences to build dynamic programs.

The `for` loop is a versatile tool for working with sequences. Experiment with different sequences and loop behaviors to master this concept!
