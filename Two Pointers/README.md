# Two Pointers

## What is it?
The **Two Pointers** technique involves iterating through a linear data structure (usually an array, string, or linked list) with two pointers moving simultaneously. By intelligently shifting the pointers based on a condition, you can drastically reduce the search space.

## How to Identify It
Look for these signals:
- **"Sorted Array" + "Find a pair"**: E.g., Two Sum II. Moving pointers from opposite ends ($L$ and $R$).
- **"In-place" modifications**: E.g., removing duplicates or moving zeroes. Use a `Read` pointer and a `Write` pointer.
- **"Find a cycle" or "Middle element" in a Linked List**: The Fast & Slow pointers (Tortoise and Hare) variation.
- **"Palindrome"**: Checking symmetry from the center outward, or edges inward.

## What is the Core Optimization?
A brute force pair-finding algorithm tests all pairs using nested loops ($O(N^2)$). Two Pointers takes advantage of sorting (or spatial relationships) to eliminate large chunks of invalid pairs in a single step, reducing the time complexity to $O(N)$.

## Progression Guide

### 1. `_must_do` (The Core Mechanics)
- **Reverse Linked List**: Master moving `prev`, `curr`, and `next` pointers.
- **3Sum**: The ultimate test of sorting + collision pointers. Fix one element, two-pointer the rest.
- **Find the Duplicate Number**: Introduces Fast & Slow pointers (Floyd's Cycle Detection) applied to an array.

### 2. `_practice` (Variations)
- **Container with Most Water**: Using two pointers to maximize area. Move the pointer pointing to the shorter line.
- **Sort Colors**: The Dutch National Flag problem. Uses 3 pointers (`low`, `mid`, `high`) to partition an array in a single pass.
- **Palindrome Linked List**: Combines finding the middle (Fast/Slow) with reversing the second half.

### 3. `_advanced` (Hard Constraints & Combinations)
- **Trapping Rain Water**: Pre-computing max-left arrays OR using two pointers intelligently from the edges.
- **Reverse Nodes in k-Group**: Complex pointer manipulation in linked lists. Maintain state across $K$ nodes.
- **Linked List Cycle II**: Floyd's Cycle Detection math to find the start of a cycle.
