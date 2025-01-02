---
layout: default
title: "Iterables & Iterators"
order: 58
---

Understanding the difference between iterables and iterators is key to working with loops and comprehensions.

### Iterables

An object that can return an iterator (e.g., lists, strings, dictionaries).

Example:

```python
my_list = [1, 2, 3]
for item in my_list:
    print(item)
```

### Iterators

An object representing a stream of data, obtained using `iter()`.

Example:

```python
my_list = [1, 2, 3]
iterator = iter(my_list)

print(next(iterator))  # 1
print(next(iterator))  # 2
```

### Expected Output

```plaintext
1
2
3
1
2
```

Mastering these concepts will deepen your understanding of Python's for-loops and data processing.
