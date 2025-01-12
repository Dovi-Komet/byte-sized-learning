---
layout: default
title: "List Operations"
order: 20
---

Python lists offer a variety of operations to manipulate and interact with the data they hold. These operations make lists one of the most flexible and powerful data structures in Python.

## Adding Elements to a List

### Using `append()`
The `append()` method adds a single element to the end of the list.

```python
fruits = ["apple", "banana"]
fruits.append("cherry")
print(fruits)
```

### Output:
```plaintext
["apple", "banana", "cherry"]
```

### Using `extend()`
The `extend()` method adds multiple elements to the end of the list.

```python
fruits = ["apple", "banana"]
fruits.extend(["cherry", "date"])
print(fruits)
```

### Output:
```plaintext
["apple", "banana", "cherry", "date"]
```

### Using `insert()`
The `insert()` method adds an element at a specified index.

```python
fruits = ["apple", "banana"]
fruits.insert(1, "cherry")
print(fruits)
```

### Output:
```plaintext
["apple", "cherry", "banana"]
```

## Removing Elements from a List

### Using `remove()`
The `remove()` method removes the first occurrence of a specified element.

```python
fruits = ["apple", "banana", "cherry"]
fruits.remove("banana")
print(fruits)
```

### Output:
```plaintext
["apple", "cherry"]
```

### Using `pop()`
The `pop()` method removes and returns an element at a specified index. If no index is specified, it removes the last element.

```python
fruits = ["apple", "banana", "cherry"]
removed_fruit = fruits.pop(1)
print(f"Removed: {removed_fruit}")
print(fruits)
```

### Output:
```plaintext
Removed: banana
["apple", "cherry"]
```

### Using `clear()`
The `clear()` method removes all elements from the list.

```python
fruits = ["apple", "banana", "cherry"]
fruits.clear()
print(fruits)
```

### Output:
```plaintext
[]
```

## Other Useful Operations

### Checking if an Element Exists
You can use the `in` keyword to check if an element exists in the list.

```python
fruits = ["apple", "banana", "cherry"]
print("banana" in fruits)
```

### Output:
```plaintext
True
```

### Getting the Length of a List
The `len()` function returns the number of elements in the list.

```python
fruits = ["apple", "banana", "cherry"]
print(len(fruits))
```

### Output:
```plaintext
3
```

---

In the next lesson, we’ll explore another type of collection: tuples.
