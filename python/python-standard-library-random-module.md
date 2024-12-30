---
layout: default
title: "Python Standard Library: `random` Module"
order: 35
---

The `random` module provides functions for generating random numbers and selecting random items.

### Generating Random Numbers

Use `random.randint()` to generate a random integer within a range.

Example:

```python
import random
number = random.randint(1, 100)
print("Random number:", number)
```

### Expected Output

```plaintext
Random number: 42  # (The actual number will vary.)
```

### Choosing a Random Item

Use `random.choice()` to select a random item from a list.

Example:

```python
colors = ["red", "blue", "green", "yellow"]
random_color = random.choice(colors)
print("Random color:", random_color)
```

### Expected Output

```plaintext
Random color: blue  # (The actual output will vary.)
```

The `random` module is useful for simulations, games, and randomized testing.