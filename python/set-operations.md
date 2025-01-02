---
layout: default
title: "Set Operations"
order: 24
---

Sets support a variety of operations that are useful for working with collections of unique items.

### Union of Sets

The union of two sets contains all unique items from both sets.

Example:

```python
set1 = {1, 2, 3}
set2 = {3, 4, 5}
union_set = set1.union(set2)
print(union_set)
```

### Expected Output

```plaintext
{1, 2, 3, 4, 5}
```

### Intersection of Sets

The intersection contains only the items that are present in both sets.

Example:

```python
intersection_set = set1.intersection(set2)
print(intersection_set)
```

### Expected Output

```plaintext
{3}
```

### Difference of Sets

The difference contains items that are in the first set but not in the second.

Example:

```python
difference_set = set1.difference(set2)
print(difference_set)
```

### Expected Output

```plaintext
{1, 2}
```