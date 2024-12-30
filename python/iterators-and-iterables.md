---
layout: default
title: "Iterators and Iterables"
order: 55
---

In Python, iterables are objects that can be looped over, and iterators are objects that enable looping by providing one element at a time.

### Iterables and the `iter()` Function

An iterable is any object that can return its elements one at a time.

Example:

```python
numbers = [1, 2, 3]
iterator = iter(numbers)
print(next(iterator))
print(next(iterator))
```

### Expected Output

```plaintext
1
2
```

### Iterators in Classes

You can define custom iterators in your classes using the `__iter__` and `__next__` methods.

Example:

```python
class Counter:
    def __init__(self, limit):
        self.limit = limit
        self.current = 0

    def __iter__(self):
        return self

    def __next__(self):
        if self.current < self.limit:
            self.current += 1
            return self.current
        raise StopIteration

counter = Counter(3)
for num in counter:
    print(num)
```

### Expected Output

```plaintext
1
2
3
```

Iterators provide fine-grained control over how data is accessed.
