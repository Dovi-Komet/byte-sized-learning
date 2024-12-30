---
layout: default
title: "Lists: Operations"
order: 17
---

You can perform many operations on lists. Let’s explore some common ones.

### Adding Items to a List

Use the `append()` method to add an item to the end of a list.

Example:

```python
fruits = ["apple", "banana"]
fruits.append("cherry")
print(fruits)
```

### Expected Output

```plaintext
['apple', 'banana', 'cherry']
```

### Removing Items from a List

Use the `remove()` method to remove a specific item.

Example:

```python
fruits = ["apple", "banana", "cherry"]
fruits.remove("banana")
print(fruits)
```

### Expected Output

```plaintext
['apple', 'cherry']
```

### Looping Through a List

You can use a `for` loop to iterate through all the items in a list.

Example:

```python
for fruit in fruits:
    print(fruit)
```

### Expected Output

```plaintext
apple
cherry
```