---
layout: default
title: "random Module"
order: 38
---

The `random` module provides functions for generating random numbers, selecting random items, and performing random operations. It is a powerful tool for simulations, games, and testing.

---

## Generating Random Numbers

Use `random.randint()` to generate a random integer within a specified range (inclusive of both ends).

### Example: Generating a Random Integer

```python
import random

number = random.randint(1, 100)  # Random integer between 1 and 100
print("Random number:", number)
```

### Output (varies):

```plaintext
Random number: 42  # (The actual number will vary.)
```

---

## Generating Random Floating-Point Numbers

Use `random.uniform()` to generate a random floating-point number within a range.

### Example: Generating a Random Float

```python
random_float = random.uniform(0, 1)  # Random float between 0 and 1
print("Random float:", random_float)
```

### Output (varies):

```plaintext
Random float: 0.572391  # (The actual output will vary.)
```

---

## Choosing Random Items

Use `random.choice()` to select a random item from a sequence like a list.

### Example: Choosing a Random Item

```python
colors = ["red", "blue", "green", "yellow"]
random_color = random.choice(colors)
print("Random color:", random_color)
```

### Output (varies):

```plaintext
Random color: blue  # (The actual output will vary.)
```

---

## Shuffling a List

Use `random.shuffle()` to randomly reorder the items in a list.

### Example: Shuffling a List

```python
numbers = [1, 2, 3, 4, 5]
random.shuffle(numbers)
print("Shuffled list:", numbers)
```

### Output (varies):

```plaintext
Shuffled list: [3, 1, 5, 2, 4]  # (The actual output will vary.)
```

---

## Generating Random Samples

Use `random.sample()` to select multiple unique random items from a sequence.

### Example: Random Sampling

```python
sample = random.sample(range(1, 10), 3)  # Select 3 unique numbers from 1 to 9
print("Random sample:", sample)
```

### Output (varies):

```plaintext
Random sample: [7, 2, 5]  # (The actual output will vary.)
```

---

## Summary

- **`random.randint(a, b)`**: Generate a random integer between `a` and `b` (inclusive).
- **`random.uniform(a, b)`**: Generate a random float between `a` and `b`.
- **`random.choice(seq)`**: Select a random item from a sequence.
- **`random.shuffle(seq)`**: Shuffle the items in a list randomly.
- **`random.sample(seq, k)`**: Select `k` unique random items from a sequence.

The `random` module is a versatile tool for adding randomness to your programs. Practice using these functions to understand their applications in various scenarios.
