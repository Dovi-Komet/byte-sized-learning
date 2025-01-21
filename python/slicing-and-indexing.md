---
title: "Slicing and Indexing"
order: 8
---

# Slicing and Indexing

Python provides powerful tools for working with sequences like strings, lists, and tuples. **Indexing** allows you to access individual elements, while **slicing** enables you to extract a portion of the sequence.

## Indexing

Indexing retrieves a single element from a sequence using its position.

### Zero-Based Indexing
- Python indices start at `0` for the first element.
- Negative indices count from the end of the sequence.

### Examples:
```python
text = "Python"

# Positive Indexing
print(text[0])  # 'P' (First character)
print(text[3])  # 'h' (Fourth character)

# Negative Indexing
print(text[-1])  # 'n' (Last character)
print(text[-3])  # 't' (Third character from the end)
```

### IndexError
Trying to access an index that doesn't exist will raise an `IndexError`:
```python
print(text[10])  # Error: Index out of range
```

---

## Slicing

Slicing extracts a subset of elements from a sequence. It uses the syntax:
```python
sequence[start:stop:step]
```
- **`start`**: The index to begin the slice (inclusive).
- **`stop`**: The index to end the slice (exclusive).
- **`step`**: The interval between indices (optional).

### Examples:
```python
text = "Python"

# Basic Slicing
print(text[0:3])  # 'Pyt' (Indices 0, 1, 2)
print(text[2:])   # 'thon' (From index 2 to the end)
print(text[:4])   # 'Pyth' (From start to index 3)

# Negative Indices
print(text[-4:])  # 'thon' (Last 4 characters)
print(text[:-2])  # 'Pyth' (Excluding the last 2 characters)

# Step
print(text[::2])  # 'Pto' (Every second character)
print(text[::-1]) # 'nohtyP' (Reversed string)
```

---

## Slicing on Other Sequences

Slicing works with any sequence type, such as **lists** and **tuples**.

### List Example:
```python
numbers = [0, 1, 2, 3, 4, 5]

# Slice
print(numbers[1:4])  # [1, 2, 3]
print(numbers[:3])   # [0, 1, 2]

# Step
print(numbers[::2])  # [0, 2, 4]

# Reverse
print(numbers[::-1]) # [5, 4, 3, 2, 1, 0]
```

### Tuple Example:
```python
data = (10, 20, 30, 40, 50)

# Slice
print(data[2:])  # (30, 40, 50)
```

---

## Common Use Cases

1. **Extracting Substrings**:
   ```python
   greeting = "Hello, World!"
   print(greeting[7:12])  # 'World'
   ```

2. **Reversing a Sequence**:
   ```python
   name = "Alice"
   print(name[::-1])  # 'ecilA'
   ```

3. **Skipping Elements**:
   ```python
   sequence = "ABCDEFGHI"
   print(sequence[::2])  # 'ACEGI'
   ```

---

## Practice Exercises

1. Given the string `"programming"`:
   - Extract `"gram"`.
   - Reverse the string.
   - Extract every third character.

2. Create a list of numbers from `1` to `10`:
   - Slice to get the first 5 numbers.
   - Slice to get the last 3 numbers.
   - Slice with a step of 2.

3. Given the tuple `(100, 200, 300, 400, 500)`:
   - Extract the middle three values.
   - Reverse the tuple.

With slicing and indexing, you can manipulate sequences efficiently and extract the data you need!
