# 1-D Dynamic Programming

## What is it?
Dynamic Programming (DP) is an optimization strategy for solving complex problems by breaking them down into simpler overlapping subproblems. **1-D DP** deals with problems where the state at any step depends strictly on a single sequence or array, meaning we only need a 1-Dimensional array or just a few variables to cache (memoize) previous states.

## How to Identify It
Look for these signals:
- **"Maximize / Minimize" or "Find the total number of ways"**: These are classic optimization/combinatorics queries.
- **"Can't be adjacent"**: E.g., House Robber. Hints at a state transition like `dp[i] = max(dp[i-1], nums[i] + dp[i-2])`.
- **"Longest sequence"**: Usually Longest Increasing Subsequence (LIS) variations.
- **Decisions at every iterative step**: "Take it or leave it" scenarios on an array.

## What is the Core Optimization?
A recursive brute force explores all possible subsets branching out, leading to $O(2^N)$ time complexity. 1-D DP identifies that many recursive branches calculate the exact same subproblem. By caching (Memoization) or building up from the start iteratively (Tabulation), we cut the time down to $O(N)$ or $O(N^2)$, trading a little memory for exponential speed.

## Progression Guide

### 1. `_must_do` (The Core Mechanics)
These lay the absolute foundation for state transitions.
- **House Robber I**: The quintessential introduction to `dp[i] = max(take, skip)`.
- **Coin Change**: Classic unbounded knapsack. Finding the minimum elements to reach a sum.
- **Standard LIS**: Understanding $O(N^2)$ DP array building based on relative ordering.

### 2. `_practice` (Variations)
- **Target Sum**: Transitioning from pure recursion to Memoization with offsets.
- **Partition Equal Subset Sum**: Using 1-D DP to simulate 0/1 Knapsack constraints.
- **Subset Sum**: Variations of building target totals.

### 3. `_advanced` (Hard Constraints & Combinations)
- **Last Stone Weight II**: Converting a physical interaction game into a Mathematical 0/1 Knapsack problem.
- **Russian Doll Envelopes**: Combining 2D Sorting with 1-D LIS (can be optimized to $O(N \log N)$ using Binary Search + DP!).
- **Ones and Zeroes**: Multi-dimensional constraints applied over a 1-D sequence constraint.
