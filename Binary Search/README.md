# Binary Search

## What is it?
Binary Search is a divide-and-conquer algorithm that finds the position of a target value within a **sorted** array. It works by repeatedly dividing the search interval in half. 

However, advanced Binary Search isn't just for finding elements. It's used to **Binary Search on an Answer**—finding the optimal value that satisfies a monotonic condition.

## How to Identify It
Look for these signals:
- **"Sorted Array" + require $O(\log N)$ Time**: This is a direct mandate to use Binary Search.
- **"Find the Minimum/Maximum" optimal value**: e.g., "minimum capacity to ship within D days". This hints at Binary Search on the Answer.
- **Monotonic functions**: If a state flips from `False` to `True` at an exact threshold, and stays `True` forever after, you can binary search for that boundary.

## What is the Core Optimization?
Instead of a linear scan $O(N)$ to find an element or test an answer, you cut the search space in half at every step. This reduces the time complexity to $O(\log N)$ or $O(N \log M)$ (when validating an answer takes $O(N)$).

## Progression Guide

### 1. `_must_do` (The Core Mechanics)
- **Find Target in Sorted Array**: The classic implementation. Master the `while (L <= R)` template.
- **Search Insert Position**: Finding the exact insertion point (usually returning `L`).
- **Search in Rotated Sorted Array**: Binary search with an extra `if` condition to determine which half is properly sorted.

### 2. `_practice` (Variations)
- **Find Minimum in Rotated Sorted Array**: A variation of the rotated logic focused on finding the pivot point.
- **Single Element in Sorted Array**: Binary searching based on even/odd index pairs rather than values.
- **Koko Eating Bananas**: The gateway to "Binary Search on Answer". Here, your array is the range of possible eating speeds `[1, max(piles)]`.

### 3. `_advanced` (Hard Constraints & Combinations)
- **Split Array Largest Sum**: Binary searching a theoretical answer (the max sum).
- **Find in Mountain Array**: Ternary search concepts mapped to Binary Search (finding the peak, then searching the slopes).
- **Median of Two Sorted Arrays**: Finding a partition point across two arrays simultaneously in $O(\log(\min(N,M)))$.

## Pro Tip
If the search space is large ($10^9$) but the condition is monotonic (e.g., "If I can ship X, I can definitely ship X+1"), **Binary Search on the Answer**. Define your `check(mid)` function first, then wrap the template around it.
