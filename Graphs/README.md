# Graphs

## What is it?
A **Graph** is a non-linear data structure consisting of nodes (vertices) connected by edges. They can be directed or undirected, weighted or unweighted. Graphs are incredibly versatile and model real-world networks like social connections, maps, and internet routing.

## How to Identify It
Look for these signals:
- **"Shortest path" or "Minimum steps"**: Usually implies Breadth-First Search (BFS) for unweighted graphs, or Dijkstra's for weighted.
- **"Connectivity", "Number of components", or "Islands"**: Implies Depth-First Search (DFS) or Union-Find (Disjoint Set).
- **"Dependencies", "Course Schedule", "Prerequisites"**: Strongly indicates Topological Sort (Kahn's Algorithm or DFS with states).

## What is the Core Optimization?
Instead of brute-forcing all possible paths which scales exponentially, Graph traversal algorithms meticulously track "visited" nodes yielding $O(V + E)$ time complexity (Vertices + Edges). For connectivity queries, **Union-Find** aggressively flattens tree structures giving near $O(1)$ amortized lookup times via Path Compression.

## Progression Guide

### 1. `_must_do` (The Core Mechanics)
- **Number of Islands**: The absolute fundamental 2D Grid DFS problem. Learn the bounds-checking bounds.
- **Rotten Oranges**: Perfecting Multi-Source BFS on a grid.
- **Number of Provinces**: Core introduction to the Union-Find data structure array.

### 2. `_practice` (Variations)
- **Topological Sort**: Mastering in-degree arrays for dependency resolution.
- **Shortest Path in Binary Matrix**: BFS with 8 directional movements.
- **Redundant Connection**: Cycle detection using Union-Find on undirected graphs.

### 3. `_advanced` (Hard Constraints & Combinations)
- **Word Ladder**: Abstracting non-obvious states (words) into a graph and running BFS.
- **Dijkstra's Shortest Path**: Handling weighted edges with a Min-Heap.
- **Accounts Merge**: Tricky strings-to-IDs mapping paired with Union-Find components.
