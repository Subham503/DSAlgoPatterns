# Math & Geometry

## What is it?
**Math & Geometry** problems test your ability to convert mathematical concepts, spatial reasoning, and 2-D coordinates into code. This includes manipulating matrices, testing prime numbers, evaluating Euclidean distances, or determining convex hulls.

## How to Identify It
Look for these signals:
- **"Rotate a matrix by 90 degrees" or "Traverse Spirally"**: Directly points to Matrix Operations involving coordinate swaps.
- **"Greatest Common Divisor" or "Prime Factorization"**: Pure Number Theory operations (Euclidean algorithm, Sieve of Eratosthenes).
- **"Closest points" or "Intersection area"**: Requires Euclidean geometry, often paired with Heaps or pure math logic.
- **Rules similar to Conway's Game of Life**: Cellular Automata matrix manipulation.

## What is the Core Optimization?
Unlike traditional algorithm problems which rely heavily on specialized data structures, Math & Geometry problems usually rely on logical formulas. Instead of building massive data structures, applying a formula (e.g., Euclidean distance formula instead of searching, or using $GCD(A, B)$) drops complexities down to $O(1)$ or $O(\log(\min(A,B)))$.

## Progression Guide

### 1. `_must_do` (The Core Mechanics)
These problems ensure you can loop through 2-D arrays without crashing and write basic logical expressions.
- **Set Matrix Zeroes**: Tricky space optimization (using the first row/col as markers).
- **Rotate Image**: In-place 2D layer-by-layer swaps.
- **Prime Checks**: Classic math (checking only up to $\sqrt{N}$).

### 2. `_practice` (Variations)
- **K Closest Points to Origin**: Combining Euclidean Math (`x^2 + y^2`) with Heaps.
- **Spiral Matrix**: Four-way boundary adjustment logic.
- **GCD & LCM**: The Euclidean Algorithm for greatest common divisors.

### 3. `_advanced` (Hard Constraints & Combinations)
- **Game of Life**: Complex in-place state modifications (using temp states like `2` or `-1`).
- **Overlapping Rectangles**: Dealing with intersection boundaries and zero-area edge cases.
- **Convex Hull / Perfect Squares**: Pure advanced geometry and mathematical theorems.
