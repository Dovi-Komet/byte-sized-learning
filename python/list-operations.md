---
layout: default
title: "List Operations"
order: 19
---

Lists in Python come with many built-in operations that make them versatile and powerful. Let’s explore some common ones.

## Adding Items to a List

Use the `append()` method to add an item to the end of a list.

### Example: Using `append()`

```python
fruits = ["apple", "banana"]
fruits.append("cherry")
print(fruits)
```

### Expected Output

```plaintext
['apple', 'banana', 'cherry']
```

## Removing Items from a List

Use the `remove()` method to remove a specific item by its value. If the item isn’t in the list, Python raises a `ValueError`.

### Example: Using `remove()`

```python
fruits = ["apple", "banana", "cherry"]
fruits.remove("banana")
print(fruits)
```

### Expected Output

```plaintext
['apple', 'cherry']
```

## Looping Through a List

You can use a `for` loop to iterate through all the items in a list.

### Example: Looping Through a List

```python
fruits = ["apple", "cherry"]
for fruit in fruits:
    print(fruit)
```

### Expected Output

```plaintext
apple
cherry
```

## Inserting Items at a Specific Position

Use the `insert()` method to add an item at a specific index.

### Example: Using `insert()`

```python
fruits = ["apple", "cherry"]
fruits.insert(1, "banana")  # Add "banana" at index 1
print(fruits)
```

### Expected Output

```plaintext
['apple', 'banana', 'cherry']
```

## Removing Items by Index

Use the `pop()` method to remove an item at a specific index. If no index is provided, `pop()` removes the last item.

### Example: Using `pop()`

```python
fruits = ["apple", "banana", "cherry"]
last_fruit = fruits.pop()  # Remove the last item
print(fruits)
print("Removed item:", last_fruit)
```

### Expected Output

```plaintext
['apple', 'banana']
Removed item: cherry
```

## Checking for an Item in a List

Use the `in` keyword to check if an item exists in a list.

### Example: Using `in`

```python
fruits = ["apple", "banana", "cherry"]
print("banana" in fruits)  # True
print("grape" in fruits)   # False
```

### Expected Output

```plaintext
True
False
```

## Summary

- Use `append()` to add items to the end of a list and `insert()` to add them at specific positions.
- Remove items with `remove()` by value or `pop()` by index.
- Loop through lists with `for` to access each item.
- Check for the presence of an item using the `in` keyword.

Lists offer a wide range of operations to manage and manipulate collections of data efficiently. Explore these operations to gain confidence in handling lists!
