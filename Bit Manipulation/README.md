# Bit Manipulation

## What is it?
**Bit Manipulation** is the act of algorithmically manipulating bits (0s and 1s) directly. Since all data is stored as bits at the hardware level, performing logic at this level bypasses high-level abstractions like arrays or looping, offering hyper-efficient operations.

## How to Identify It
Look for these signals:
- **"Find the missing number" or "Find the element appearing only once"**: The classic XOR signal ($a \oplus a = 0$).
- **"Represent combinations"**: E.g., choosing subsets of an array size $N < 32$. An integer mathematically acts as a fixed array of booleans.
- **Mathematical constraints forbidding $+, -, *, /$**: Requires recreating arithmetic logic gates using `&` (AND), `|` (OR), `^` (XOR), and `<<` (Shifts).

## What is the Core Optimization?
Bitwise operations execute typically in 1 CPU cycle. Using an integer as a Set ("Bitmask") to track combinations transforms expensive Array-allocation Backtracking ($O(2^N \cdot N)$ Space/Time) into simple Bitwise-shifts ($O(2^N)$ Time, $O(1)$ Space).

## Progression Guide

### 1. `_must_do` (The Core Mechanics)
- **Single Number**: The "Hello World" of XOR operations. 
- **Power of Two**: The definitive `n & (n - 1) == 0` trick.
- **Subset Generation**: Iterate from $0$ to $2^N-1$. Treat every bit of the iterator as a booean flag for the array elements!

### 2. `_practice` (Variations)
- **Reverse Bits**: Masking and shifting bits efficiently.
- **Add Without Arithmetic Operators**: Simulating half-adders/full-adders in software using XOR and AND.
- **XOR Queries of a Subarray**: Extending Prefix Sums to Prefix XORs.

### 3. `_advanced` (Hard Constraints & Combinations)
- **N-Queens (Bitmask)**: Evolving array-based backtracking into sheer wizardry by using 3 integers to track conflicts diagonally.
- **Maximum Product of Word Lengths**: Representing 26 lowercase English letters as 26 bits to do $O(1)$ intersection tests.
- **Find Original Array of Prefix XOR**: Mathematical unraveling of cumulative XOR operations.
