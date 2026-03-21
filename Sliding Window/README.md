# Sliding Window Pattern

## What is it?
The **Sliding Window** is a technique used to perform operations on a specific window size of a given array or linked list, such as finding the longest subarray containing all 1s. Sliding Windows are useful for solving problems that ask for subarrays or substrings satisfying a certain condition.

## When to Use (Heuristics)
Use Sliding Window when you encounter these signals:
- Given an **Array** or **String**.
- Asked to find a **Contiguous Subarray** or **Substring**.
- Looking for **maximum**, **minimum**, **longest**, **shortest**, or a specific **Sum/Target**.

## The Two Types
1. **Fixed Size**: The window size $K$ remains constant. You add one element to the right and remove one from the left.
2. **Variable Size**: The window grows to the right until a condition breaks, then shrinks from the left until the condition is valid again.

## Progression Guide

### 🟢 `_must_do/`
The foundational problems that teach the core mechanics. Start here.
- Maximum Sum Subarray of Size K (Fixed)
- Longest Substring Without Repeating Characters (Variable)

### 🟡 `_practice/`
Core variants testing your ability to adapt the window condition.
- Permutation in String (Fixed + Hash Map)
- Longest Repeating Character Replacement (Variable)

### 🔴 `_advanced/`
Complex conditions, often requiring Monotonic Queues, Deques, or multiple pointers.
- Sliding Window Maximum (Monotonic Queue)
- Sliding Subarray Beauty

## Pro Tip
Always define clearly:
1. When to expand the window (`right++`).
2. When the window violates the condition.
3. When and how to shrink the window (`left++`).
