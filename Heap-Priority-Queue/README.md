# Heap / Priority Queue

*Note: Monotonic Stacks and generic combinations are found in "Heap, Merge, & Stacks". This folder focuses purely on Heaps.*

## What is it?
A **Heap** (Priority Queue) is a complete binary tree that maintains the Heap Property: The parent is always greater/smaller than its children. It guarantees $O(1)$ access to the absolute highest/lowest priority element and $O(\log N)$ insertions/deletions.

## How to Identify It
Look for these signals:
- **"Top K items" or "Kth largest/smallest"**: By maintaining a Min-Heap of size K, you guarantee the peak element is the answer in $O(N \log K)$.
- **"Stream of data"**: Continually finding the max/min of incoming live data.
- **"Dijkstra's Algorithm" or "Prim's Algorithm"**: Weighted graph traversals inherently demand a priority queue to fetch the next shortest edge.

## What is the Core Optimization?
Sorting an array to find top elements takes $O(N \log N)$ initially. If the data is dynamic (streaming), re-sorting after every insertion is an $O(N^2 \log N)$ disaster. Heaps guarantee $O(\log N)$ structural maintenance allowing extreme efficiency on streaming architectures.

## Progression Guide

### 1. `_must_do` (The Core Mechanics)
- **Last Stone Weight**: Simple heap simulation. Pop two, push the difference.
- **Kth Largest Element in a Stream**: The gateway to keeping a fixed-size Min-Heap.

### 2. `_practice` (Variations)
- **Kth Largest Element in an Array**: Introduces heapify $O(N)$ operations for static arrays versus naive insertions.

### 3. `_advanced` (Hard Constraints & Combinations)
- **Task Scheduler**: Heaps paired with cooldown queues (simulating CPU cycles).
- **Merge K Sorted Lists**: A fundamental $O(N \log K)$ merging algorithm.
- **Find Median from Data Stream**: The legendary Two-Heaps problem (balancing a Max-Heap for the left half and a Min-Heap for the right half).
