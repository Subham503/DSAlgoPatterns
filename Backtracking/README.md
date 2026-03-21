# Backtracking

## What is it?
Backtracking is an algorithmic technique for solving problems recursively by trying to build a solution incrementally, one piece at a time. If it realizes that the current path cannot possibly lead to a valid solution, it abandons it ("backtracks") and tries the next option. It is a refined, optimized form of brute force searching.

## How to Identify It
Look for these signals:
- **"Find all possible..."**: Whenever a problem asks for *all* combinations, permutations, subsets, or ways to arrange items.
- **"Return a list of all valid..."**: e.g., Sudoku solvers, N-Queens variations.
- **Constraints are remarkably small (N < 20)**: Backtracking is usually $O(2^N)$ or $O(N!)$. If the input size is tiny, it's almost certainly Backtracking.

## What is the Core Optimization?
Instead of generating every single possible state (Pure Brute Force) and then filtering out the invalid ones, Backtracking filters *during* the generation process. This is called **Pruning**. If branching down a path violates a constraint, you immediately `return` instead of going deeper.

## Progression Guide

### 1. `_must_do` (The Core Mechanics)
These problems establish the fundamental "Choose -> Explore -> Unchoose" template.
- **Subsets**: The basic binary choice (include vs exclude).
- **Generate Parentheses**: Backtracking with a running state (open vs closed brackets).
- **Permutations**: The classic $O(N!)$ traversal.

### 2. `_practice` (Variations)
- **Combination Sum I & II**: Navigating target sums with or without bounded usage of array elements.
- **Word Search**: Backtracking over a 2D matrix (DFS + State Reversal).

### 3. `_advanced` (Hard Constraints & Combinations)
- **Palindrome Partitioning**: Combining Backtracking with string substring validation.
- **Sudoku Solver & N-Queens**: The ultimate constraint-satisfaction problems involving complex board-state maintenance.
