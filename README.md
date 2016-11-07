# algorithms-cheat-sheet {

## Important Data Structures

### Linked Lists

### Stacks + Queues

### Trees

### n-ary Tree

An n-ary tree is a tree where each node in the tree can have at most *n* children.

#### Binary Search Tree (BST)

*Binary Search Tree Conditions*: The left subtree of a node contains only values less than or equal to the node's value. The right subtree of a node contains only values greater than or equal to the node's value. Both the left and right subtrees are BSTs

Basic operations (search, insert, delete) on BSTs take **O(log n)** time. 

### Heaps

- Can be implemented using an n-ary tree or an array
- If implemented using a tree, the heap must be filled from top to bottom, left to right

*Min-Heap Condition*: The key stored at each node must be <= to the keys of its children

*Max-Heap Condition*: The key stored at each node must be >= to the keys of its children

#### Implementing a heap as a tree

A heap implemented using a tree must be an n-ary tree where each level down to the maximum depth level must be **completely** full and the bottom level must be filled from left to right, with no gaps occuring.

#### Implementing a heap as an array

A heap implemented as an array has the property where each index *n* has children at *2n + 1* and *2n + 2*, for all *n* >= 0.

#### Adding to Heap

> Applies to max-heap

Add to the bottom-most, right-most empty position. Check if the new node is greater than it's parent. If it is, then you switch the valus and perform the check again until the parent is greater than thenew node or the parent is null (meaning that we've reached the root).

#### Removing from the heap

> Applies to max-heap

We usually want to remove the root node of the heap (highest priority in the priority queue). If we remove the root node, we must find the most recently inserted node (i.e. the bottom-most, right-most node in the tree) and replace the root node with that node. We must then verify that the heap still satisfies the max-heap condition, by comparing the new root node to its children. If one or more of the children is greater than the new node, we switch the new value with the largest of those children and performt he check again on the new children of the new node. If no such child exists, then the max-heap condition is satisfied.

### Hash Tables

## Algorithms

### Breadth-First Search

### Depth-First Search

### Binary Search

> **Time Complexity:** O(log n)
>
> **Space Complexity:** O(1)

To perform binary search, you must have a sorted list (or array). Since the list is sorted, we are able to look at the value in the middle of the list and compare it to the value that we are looking for. If the value is the same as the value in the middle of the list, then we have found the value that we're looking for. If the value is less than the value we are looking for, then we know the that the value must be in the sub-array to the right of the value. If the value is larger than the value we are looking for, then we know that the value must be in the sub-array to the left of the value. If the value is not the value we are looking for, then we perform binary search recursively on the aforementioned sub-array.

### Merge Sort

### Quicksort

### Insertion Sort

# }
