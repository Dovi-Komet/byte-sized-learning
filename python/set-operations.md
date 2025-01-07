---
layout: default
title: "Set Operations"
order: 25
---

Sets in Python support a variety of operations that are useful for working with collections of unique items. These operations make sets ideal for tasks involving comparisons and mathematical set logic.

## Union of Sets

The union of two sets contains all unique items from both sets. Use the `union()` method or the `|` operator.

### Example: Union

```python
set1 = {1, 2, 3}
set2 = {3, 4, 5}
union_set = set1.union(set2)
print(union_set)
```

### Output

```plaintext
{1, 2, 3, 4, 5}
```

You can achieve the same result using the `|` operator:

```python
union_set = set1 | set2
print(union_set)
```

## Intersection of Sets

The intersection contains only the items that are present in both sets. Use the `intersection()` method or the `&` operator.

### Example: Intersection

```python
intersection_set = set1.intersection(set2)
print(intersection_set)
```

### Output

```plaintext
{3}
```

You can also use the `&` operator:

```python
intersection_set = set1 & set2
print(intersection_set)
```

## Difference of Sets

The difference contains items that are in the first set but not in the second. Use the `difference()` method or the `-` operator.

### Example: Difference

```python
difference_set = set1.difference(set2)
print(difference_set)
```

### Output

```plaintext
{1, 2}
```

The `-` operator produces the same result:

```python
difference_set = set1 - set2
print(difference_set)
```

## Symmetric Difference of Sets

The symmetric difference contains items that are in either set, but not in both. Use the `symmetric_difference()` method or the `^` operator.

### Example: Symmetric Difference

```python
symmetric_difference_set = set1.symmetric_difference(set2)
print(symmetric_difference_set)
```

### Output

```plaintext
{1, 2, 4, 5}
```

The `^` operator achieves the same result:

```python
symmetric_difference_set = set1 ^ set2
print(symmetric_difference_set)
```

## Summary

- **Union (`union()` or `|`)**: Combines all unique items from both sets.
- **Intersection (`intersection()` or `&`)**: Finds common items in both sets.
- **Difference (`difference()` or `-`)**: Finds items in the first set but not in the second.
- **Symmetric Difference (`symmetric_difference()` or `^`)**: Finds items in either set but not in both.

These operations make sets a powerful tool for comparing and combining collections. Experiment with these operations to understand how they can simplify your code.
