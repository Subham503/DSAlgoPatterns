# Greedy & Design

## What is it?
This combined category tests two distinct, advanced paradigms:
1. **Greedy Algorithms**: Making the locally optimal choice at each stage with the hope of finding a global optimum. You never "re-evaluate" previous choices (no backtracking or DP).
2. **System Design (Data Structures)**: Building custom classes/systems that maintain precise constraints over time, simulating real-world architectures.

## How to Identify It
Look for these signals:
- **"Maximum profit", "Minimum jumps", "Largest sum"**: Seems like DP, but if you can confidently take the "best" available option without negative consequences, it's Greedy.
- **"Return the `min` / `max` / `count` with $O(1)$ requirements"**: You are being asked to *Design* a data structure combining HashMaps and Doubly Linked Lists or equivalent fast storage.
- **"Implement `class X` with methods `get`, `put`, `remove`"**: Immediate marker of a Design problem.

## What is the Core Optimization?
- **Greedy**: Transforms $O(2^N)$ backtracking or $O(N^2)$ DP down to a single pass ($O(N)$ or $O(N \log N)$ with sorting).
- **Design**: Fusing multiple data structures (like a `HashMap` mapping to a `Doubly Linked List` node) gives $O(1)$ operations where normally elements would need to be searched $O(N)$.

## Progression Guide

### 1. `_must_do` (The Core Mechanics)
- **Jump Game II**: The definitive Greedy pathfinding problem.
- **Gas Station**: Elegant single-pass validation via a cumulative sum.
- **LRU Cache**: The classic combination of a Hash Map and Doubly Linked List for $O(1)$ eviction.

### 2. `_practice` (Variations)
- **Boats to Save People**: Greedy paired with Two-Pointers (pair the heaviest with the lightest).
- **Design Browser History**: Tracking history with bounded stacks or pointer arrays.
- **Design Circular Deque**: Circular pointer management.

### 3. `_advanced` (Hard Constraints & Combinations)
- **Wiggle Subsequence & Candy**: Non-intuitive greedy logic requiring peaks, valleys, and left/right sweeps.
- **LFU Cache**: Upgrading LRU logic to track *frequencies* (requires Maps of Lists or Priority Queues).
- **Design Twitter**: Object-oriented design simulating complex timelines with multi-way merges.
