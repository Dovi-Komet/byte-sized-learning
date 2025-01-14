---
layout: default
title: "Sorting & Keys"
order: 50
---

Sorting is a fundamental operation in programming, and Python provides powerful tools for sorting data. You can sort lists and other iterable data types using the `sorted()` function or the `sort()` method. Both can be customized with a **key function**.

---

## Sorting with `sorted()`

The `sorted()` function creates a new sorted list from any iterable.

### Example: Sorting a List of Numbers

```python
numbers = [5, 2, 9, 1, 5, 6]
sorted_numbers = sorted(numbers)
print(sorted_numbers)  # Output: [1, 2, 5, 5, 6, 9]
```

---

## Sorting In-Place with `sort()`

The `sort()` method modifies the list in place, rather than creating a new list.

### Example: Sorting a List In-Place

```python
numbers = [5, 2, 9, 1, 5, 6]
numbers.sort()
print(numbers)  # Output: [1, 2, 5, 5, 6, 9]
```

---

## Reverse Sorting

You can sort in descending order by using the `reverse` parameter.

### Example: Sorting in Reverse Order

```python
numbers = [5, 2, 9, 1, 5, 6]
sorted_numbers = sorted(numbers, reverse=True)
print(sorted_numbers)  # Output: [9, 6, 5, 5, 2, 1]
```

---

## Custom Sorting with `key`

The `key` parameter allows you to define a custom sorting order by providing a function.

### Example: Sorting Strings by Length

```python
words = ["apple", "banana", "kiwi", "grape"]
sorted_words = sorted(words, key=len)
print(sorted_words)  # Output: ['kiwi', 'grape', 'apple', 'banana']
```

### Example: Sorting by a Custom Function

You can use any function as a key.

```python
def second_letter(word):
    return word[1]

words = ["apple", "banana", "kiwi", "grape"]
sorted_words = sorted(words, key=second_letter)
print(sorted_words)  # Output: ['banana', 'apple', 'grape', 'kiwi']
```

---

## Sorting Complex Data Structures

### Example: Sorting a List of Dictionaries

When dealing with dictionaries, you can sort based on specific keys.

```python
people = [
    {"name": "Alice", "age": 30},
    {"name": "Bob", "age": 25},
    {"name": "Charlie", "age": 35}
]

sorted_people = sorted(people, key=lambda x: x["age"])
print(sorted_people)
# Output: [{'name': 'Bob', 'age': 25}, {'name': 'Alice', 'age': 30}, {'name': 'Charlie', 'age': 35}]
```

---

## Stable Sorting

Python’s sorting is **stable**, meaning the relative order of equal elements is preserved.

---

## Key Takeaways

1. Use `sorted()` for creating a new sorted list and `sort()` for in-place sorting.
2. The `key` parameter is a powerful tool for custom sorting.
3. Python’s sorting algorithms are efficient and stable.

---

In the next lesson, we’ll dive into unit testing and how to write reliable tests for your Python programs.
