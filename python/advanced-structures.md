---
layout: default
title: "Advanced Structures"
order: 98
---

Advanced data structures like heaps, linked lists, and trees are important for interviews.

### Using Heaps with `heapq`

Example:

```python
import heapq

numbers = [5, 7, 9, 1, 3]
heapq.heapify(numbers)
print("Heap:", numbers)
print("Smallest element:", heapq.heappop(numbers))
```

### Implementing a Linked List

Example:

```python
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class LinkedList:
    def __init__(self):
        self.head = None

    def append(self, data):
        new_node = Node(data)
        if not self.head:
            self.head = new_node
        else:
            current = self.head
            while current.next:
                current = current.next
            current.next = new_node

linked_list = LinkedList()
linked_list.append(10)
linked_list.append(20)
print("First element:", linked_list.head.data)
```

### Expected Output

```plaintext
Heap: [1, 3, 9, 7, 5]
Smallest element: 1
First element: 10
```

Understanding these structures prepares you for algorithmic problem-solving.
