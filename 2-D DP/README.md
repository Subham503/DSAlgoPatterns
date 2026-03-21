# 2-D Dynamic Programming

## What is it?
**2-D Dynamic Programming** expands the concept of DP to scenarios where the state depends on *two* changing variables. This is most commonly seen when traversing a 2D grid, comparing two different strings, or evaluating sub-intervals of an array.

## How to Identify It
Look for these signals:
- **Two Strings / Arrays are given**: e.g., "Find the Longest Common Subsequence of str1 and str2." State is `(i, j)`.
- **"Paths in a Matrix"**: e.g., "Find minimum path sum from top-left to bottom-right." State is `(row, col)`.
- **"Matrix Chain Multiplication" / Partitioning**: Trying to optimally place parentheses or split arrays/palindromes. State is usually `(start_index, end_index)`.

## What is the Core Optimization?
Similarly to 1-D DP, naive recursion with two moving pointers/indices results in exponential blowup $O(3^{N+M})$ or similar. By storing results in a `matrix[i][j]`, we guarantee that each state combination is evaluated exactly once. For two strings of length $N$ and $M$, this reduces the time to $O(N \cdot M)$.

## Progression Guide

### 1. `_must_do` (The Core Mechanics)
- **Unique Paths**: The definitive gateway to Grid DP. `dp[i][j] = dp[i-1][j] + dp[i][j-1]`.
- **Longest Common Subsequence**: The absolute essential string comparison template.

### 2. `_practice` (Variations)
- **Minimum Path Sum**: Adding greedy weight matrices to the Unique Paths concept.
- **Edit Distance**: The Levenshtein distance algorithm. Master interpreting insert/delete/replace state movements.

### 3. `_advanced` (Hard Constraints & Combinations)
- **Dungeon Game**: A backward Grid DP problem where constraints (HP must be > 0 at all times) strictly enforce bottom-up calculation.
- **Interleaving String**: Tricky boolean 2D-DP state mapping.
- **Burst Balloons / Minimum Cost Tree**: Classic Matrix Chain Multiplication structures where you evaluate all possible partition points `k` between `i` and `j` ($O(N^3)$ complexity).

## Pro Tip
For "Two String" DP problems (like LCS or Edit Distance), the `dp[i][j]` state usually represents the answer for prefixes `str1[0...i]` and `str2[0...j]`. If you only need the previous row of the DP table, you can optimize space to **$O(\min(N, M))$** by using two rows instead of a full matrix.
