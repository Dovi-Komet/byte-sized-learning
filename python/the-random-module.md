---
title: "The random Module"
order: 28
---

# The `random` Module

The **`random` module** in Python is used to generate pseudo-random numbers, select random elements, and perform random operations. It is particularly useful in simulations, games, testing, and data analysis.

---

## Generating Random Numbers

### 1. Random Float Between 0 and 1
```python
import random

print(random.random())  # Output: Random float between 0.0 and 1.0
```

### 2. Random Float in a Range
```python
print(random.uniform(10, 20))  # Output: Random float between 10 and 20
```

### 3. Random Integer
```python
print(random.randint(1, 10))  # Output: Random integer between 1 and 10 (inclusive)
```

### 4. Random Integer in a Range (Step Support)
```python
print(random.randrange(0, 10, 2))  # Output: Random even number between 0 and 10 (exclusive)
```

---

## Random Choices from Sequences

### 1. Random Element from a List
```python
colors = ["red", "blue", "green", "yellow"]
print(random.choice(colors))  # Output: Random color
```

### 2. Random Multiple Choices (With Replacement)
```python
print(random.choices(colors, k=3))  # Output: List of 3 random colors (with replacement)
```

### 3. Random Sample (Without Replacement)
```python
print(random.sample(colors, k=3))  # Output: List of 3 unique random colors
```

### 4. Shuffle a List
```python
random.shuffle(colors)
print(colors)  # Output: Shuffled list
```

---

## Random Boolean

### Simulate a Coin Toss
```python
print(random.choice([True, False]))  # Output: True or False
```

---

## Seeding the Random Number Generator

By default, Python’s random number generator uses the current system time. You can seed it for reproducible results.

```python
random.seed(42)
print(random.randint(1, 10))  # Output: Same number every time the script is run
```

---

## Use Cases of `random`

### 1. Simulating a Dice Roll
```python
def roll_dice():
    return random.randint(1, 6)

print(roll_dice())  # Output: Random number between 1 and 6
```

### 2. Simulating a Lottery Draw
```python
def lottery_draw():
    return random.sample(range(1, 50), 6)

print(lottery_draw())  # Output: List of 6 unique random numbers
```

### 3. Generating a Random Password
```python
import string

def generate_password(length):
    chars = string.ascii_letters + string.digits + string.punctuation
    return ''.join(random.choices(chars, k=length))

print(generate_password(12))  # Output: Random 12-character password
```

---

## Best Practices

1. **Seeding for Reproducibility**:
   - Use `random.seed()` when you need predictable results, such as for testing or debugging.

2. **Avoid for Cryptographic Purposes**:
   - The `random` module is not suitable for cryptographic applications. Use the `secrets` module for secure random numbers.

3. **Shuffle Carefully**:
   - When shuffling, be cautious with large datasets, as it modifies the list in place.

---

## Practice Exercises

1. **Dice Simulation**:
   - Simulate rolling two six-sided dice and print their sum.

2. **Random Names**:
   - Write a script that randomly picks a name from a list of participants for a prize.

3. **Number Guessing Game**:
   - Create a game where the user has to guess a random number between 1 and 100, with hints given for "higher" or "lower."

4. **Deck Shuffling**:
   - Simulate a deck of cards, shuffle it, and deal five random cards.

The `random` module is a versatile tool for adding unpredictability to your programs. It is easy to use and provides a wide range of randomization functionalities.