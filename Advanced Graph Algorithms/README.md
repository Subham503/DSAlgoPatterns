# Advanced Graph Algorithms

## What is it?
Beyond basic traversals (BFS/DFS) and connectivity (Union-Find), **Advanced Graph Algorithms** tackle complex structural and pathing problems. These include identifying critical weaknesses in network infrastructure, finding optimal flows, or determining Eulerian paths.

## How to Identify It
Look for these signals:
- **"Critical connection", "Single point of failure"**: Points directly to Tarjan's Algorithm for Finding Bridges / Articulation Points.
- **"Visit every edge exactly once"**: Euler Path / Circuit (Hierholzer's algorithm).
- **"Bellman-Ford", "Floyd-Warshall"**: Weighted graphs with negative weights or All-Pairs Shortest Path requirements.

## What is the Core Optimization?
The naive approach to finding a "bridge" (critical connection) is to remove each edge one by one and run DFS/BFS to check connectivity, yielding an $O(E \cdot (V+E))$ time complexity. Advanced algorithms like Tarjan's use deep insight into DFS trees (tracking `discovery_time` and `lowest_reachable_time`) to solve it in a single impressive $O(V+E)$ pass.

## Progression Guide

### 1. `_must_do` (The Core Mechanics)
- **Critical Connections in a Network**: The hallmark problem for finding Bridges. Mastering the `timer` array concept.

### 2. `_practice` & `_advanced` (Variations)
*(More problems to be added as pattern evolves)*
- Identifying Articulation Points (Vertices whose removal disconnects the graph).
- Complex Negative Cycle Detection.
