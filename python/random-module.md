---
layout: default
title: "random Module"
order: 39
---

The `random` module in Python provides functions for generating random numbers and performing random operations. It is commonly used in simulations, games, data sampling, and testing.

---

## Importing the `random` Module

To use the `random` module, import it into your program:

```python
import random
```

---

## Common Functions in the `random` Module

### `random.random()`: Generate a Random Float

This function generates a random floating-point number between `0.0` (inclusive) and `1.0` (exclusive).

```python
# Generate a random float
random_float = random.random()
print("Random Float:", random_float)
```

---

### `random.randint()`: Generate a Random Integer

The `randint(a, b)` function generates a random integer between `a` and `b` (both inclusive).

```python
# Generate a random integer between 1 and 10
random_int = random.randint(1, 10)
print("Random Integer:", random_int)
```

---

### `random.choice()`: Choose a Random Element from a Sequence

The `choice()` function selects a random element from a sequence like a list or tuple.

```python
# Randomly select an element from a list
fruits = ["apple", "banana", "cherry"]
random_fruit = random.choice(fruits)
print("Random Fruit:", random_fruit)
```

---

### `random.shuffle()`: Shuffle a List

The `shuffle()` function shuffles a list in place, randomly reordering its elements.

```python
# Shuffle a list
numbers = [1, 2, 3, 4, 5]
random.shuffle(numbers)
print("Shuffled List:", numbers)
```

---

### `random.sample()`: Random Sampling

The `sample()` function selects a specified number of unique elements from a sequence.

```python
# Select 3 unique elements from a list
sampled_numbers = random.sample(range(1, 11), 3)
print("Random Sample:", sampled_numbers)
```

---

### `random.uniform()`: Generate a Random Float in a Range

The `uniform(a, b)` function generates a random floating-point number between `a` and `b`.

```python
# Generate a random float between 5.5 and 10.5
random_float_range = random.uniform(5.5, 10.5)
print("Random Float in Range:", random_float_range)
```

---

### `random.seed()`: Reproducible Randomness

The `seed()` function initializes the random number generator to produce reproducible results.

```python
# Set a seed for reproducibility
random.seed(42)
print("Random Integer (with seed):", random.randint(1, 10))
```

---

## Example: Simulating a Dice Roll

```python
import random

# Simulate rolling a dice
def roll_dice():
    return random.randint(1, 6)

print("You rolled a:", roll_dice())
```

---

## Documentation

For a full list of functions, visit the [official Python documentation](https://docs.python.org/3/library/random.html){:target="_blank"}.

---

The `random` module is a versatile tool for generating random data in Python. In the next lesson, we’ll begin our journey into Object-Oriented Programming (OOP) with the basics.
