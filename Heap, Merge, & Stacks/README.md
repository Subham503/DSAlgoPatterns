# Heap, Merge, & Stacks

## What is it?
This meta-category covers three critical secondary data structures that excel at specific constraint processing:
1. **Heaps / Priority Queues**: Trees that maintain the absolute min/max element at the root in $O(1)$ time and allow insertions in $O(\log N)$.
2. **K-Way Merge**: Using heaps to merge multiple sorted arrays.
3. **Monotonic Stacks**: A stack whose elements are strictly increasing or decreasing, used to find specific relationships like the "Next Greater Element".

## How to Identify It
Look for these signals:
- **"Top K", "Kth Largest", "K Closest"**: Immediate signal for a Heap (size K).
- **"Next greater", "Previous smaller", "Daily Temperatures"**: The canonical signal for a Monotonic Stack.
- **"Merge K sorted lists" or "Find median of a data stream"**: Advanced Heap strategies like Two-Heaps or K-Way Merge.

## What is the Core Optimization?
- **Heap**: Instead of sorting the entire array ($O(N \log N)$) to find the top K elements, you maintain a heap of size K, taking $O(N \log K)$.
- **Monotonic Stack**: Instead of an $O(N^2)$ nested loop to look ahead for the next larger element, you push elements to a stack and pop them when you find a violation of the monotonicity, maintaining $O(N)$ time.

## Progression Guide

### 1. `_must_do` (The Core Mechanics)
- **Daily Temperatures**: The definitive Monotonic Stack problem.
- **Next Greater Element II**: Handling monotonic stacks on circular arrays.
- **Ugly Number II**: Using a Min-Heap for state generation and popping the smallest dynamically.

### 2. `_practice` (Variations)
- **Largest Rectangle in Histogram**: A classic hard Monotonic Stack problem disguised as Geometry.
- **Online Stock Span**: Monotonic stacks applied to a running object/class stream.
- **IPO**: Using Two Heaps (Max-Heap for profits, Min-Heap for capital) to maximize returns greedily.

### 3. `_advanced` (Hard Constraints & Combinations)
- **Next Greater Node in Linked List**: Adapting arrays to linked lists while using monotonic stacks.
- **Maximum Width Ramp**: Complex monotonic stack variations.
- **Sliding Window Median**: Combines Sliding Window + Two Heaps!
