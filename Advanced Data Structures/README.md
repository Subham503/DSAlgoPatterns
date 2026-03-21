# Advanced Data Structures

## What is it?
**Advanced Data Structures** covers specialized trees and array abstractions that handle strictly specific, ultra-fast querying. The most prominent example is the **Segment Tree** (or Fenwick Tree / Binary Indexed Tree), which allows for dynamic, updatable array queries.

## How to Identify It
Look for these signals:
- **"Range Sum", "Range Min/Max" + "Updates are frequent"**: $O(1)$ prefix sums are great until the array changes. If an array changes out from under you, rebuilding a prefix sum array takes $O(N)$. Segment Trees handle both updates and range queries in $O(\log N)$.
- **"Count smaller/larger elements to the right"**: While solvable with modified Merge Sort, it's a classic signal for a Binary Indexed Tree tracking frequencies dynamically.

## What is the Core Optimization?
A standard array update is $O(1)$ but a range sum is $O(N)$. A prefix sum array makes a range sum $O(1)$ but an update is $O(N)$. A **Segment Tree** balances this by giving mathematically robust trees where *both* updates and range queries are strictly $O(\log N)$, enabling massive real-time data streaming architectures.

## Progression Guide

### 1. `_must_do` (The Core Mechanics)
- **Range Sum Query - Mutable**: The definitive 'Hello World' for Segment Trees and Fenwick Trees.

### 2. `_advanced` (Hard Constraints & Combinations)
- **Count of Smaller Numbers After Self**: Bounding frequency tracking inside an advanced spatial tree structure.
