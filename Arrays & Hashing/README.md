# Arrays & Hashing

## What is it?
Arrays are contiguous blocks of memory, and Hashing (Hash Maps/Sets) refers to data structures that offer $O(1)$ average time complexity for insertions, deletions, and lookups. 
Together, **Arrays & Hashing** form the most fundamental pattern in algorithms. Whenever you need to count occurrences, map elements to indices, or check if an element exists while traversing an array, a hash map is your best friend.

## How to Identify It
Look for these signals in the problem description:
- **"Find frequencies" or "Count occurrences"**: Immediately points to a Hash Map.
- **"Find a pair/subarray that sums to K"**: Points to Prefix Sums cached in a Hash Map.
- **"Contains duplicate" or "Unique elements"**: Points to a Hash Set.
- **Need $O(1)$ lookups**: Instead of nesting loops ($O(N^2)$), use a hash map to remember what you've seen so far.

## What is the Core Optimization?
Instead of a brute-force approach where you use a nested loop to compare every element against every other element ($O(N^2)$), you do a single pass over the array. During this pass, you **store** elements (or modified values like prefix sums) in a hash map. This trades $O(N)$ Space for a massive reduction to $O(N)$ Time.

## Progression Guide

### 1. `_must_do` (The Core Mechanics)
These problems establish the fundamental "Trade Space for Time" concept.
- **Two Sum**: The classic hash map problem. Store `target - current_val` as you iterate.
- **Group Anagrams**: Teaches you how to use a transformed string (sorted, or frequency array) as a hash map key.
- **Find Middle Index in Array**: Introduces Prefix Sums, a crucial technique for array queries.

### 2. `_practice` (Variations)
- **Top K Frequent Elements**: Combines Hashing with sorting/heaps/buckets.
- **Product Except Self**: Teaches prefix and postfix arrays without using division.
- **Two Sum II**: An array variation where the input is sorted (leads into Two Pointers).

### 3. `_advanced` (Hard Constraints & Combinations)
- **Maximum Product Subarray**: Introduces keeping track of both min and max to handle negative products.
- **Number of Ways to Split Array**: Advanced prefix sum manipulation.
- **Range Sum Query 2D**: Expands prefix sums into a 2D matrix.

## Pro Tip
When using a Hash Map for frequency counting, always check if you can use a fixed-size integer array `int[26]` for lowercase alphabet problems to save heap overhead and improve cache locality.
