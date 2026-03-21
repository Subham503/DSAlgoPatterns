# Linked List Pattern

## What is it?
A **Linked List** is a linear data structure where elements are not stored in contiguous memory locations. Instead, each node contains a `data` field and a `next` pointer to the next node. Mastery of linked lists is essential for understanding more complex structures like Trees and Graphs.

## How to Identify It
Look for these signals:
- **"Dynamic size requirement"**: When you need $O(1)$ insertions/deletions at the head/tail without shifting elements (unlike Arrays).
- **"Pointer manipulation"**: The problem involves "Reversing", "Merging", or "Finding a cycle".
- **Constraints specify "N nodes"**: Usually implies a single pass $O(N)$ is expected.

## What is the Core Optimization?
Unlike arrays, linked lists allow for **structural changes** (like removing a node in the middle) in $O(1)$ time *if* you already have a pointer to that node. This makes them ideal for implementation of LRU Caches, Stacks, and Queues.

## Progression Guide

### 🟢 `_must_do/`
- **Reverse Linked List**: The absolute foundation of pointer re-assignment.
- **Merge Two Sorted Lists**: Teaches traversal and the "Dummy Node" technique.
- **Linked List Cycle**: Basic Fast & Slow pointer implementation.

### 🟡 `_practice/`
- **Remove Nth Node From End**: Using two pointers with a fixed gap.
- **Copy List with Random Pointer**: Mastering deep copies of complex pointers.
- **Add Two Numbers**: Handling math across nodes with carry-over.

### 🔴 `_advanced/`
- **Reverse Nodes in k-Group**: Complex recursive or iterative nested reversal.
- **Merge K Sorted Lists**: Combining Linked Lists with Heaps to achieve $O(N \log K)$.
- **LRU Cache**: A hybrid pattern combining Doubly Linked Lists with Hash Maps.

## Pro Tip
**Always use a Dummy Node (`new Node(0)`)** as the start of your result list. It eliminates the need for annoying `if (head == null)` edge cases when building a new list from scratch. Always return `dummy.next`.
