# Trees & Trie

## What is it?
**Trees** are hierarchical data structures linking nodes via edges (usually Binary Trees where each node has up to two children). 
A **Trie** (Prefix Tree) is a specialized n-ary tree used for locating specific keys from within a set, usually strings.

## How to Identify It
Look for these signals:
- **"Level by Level" or "Shortest Depth"**: Requires BFS (Queue).
- **"Path Sum", "Max Depth", "Lowest Common Ancestor"**: Requires DFS (Recursion/Stack).
- **"Autocomplete", "Prefix Search", "Dictionary Validation"**: Screams Trie Data Structure.

## What is the Core Optimization?
- **Trees**: Allow modeling of hierarchical data and $O(\log N)$ search times if balanced (BST). Recursive DFS enables solving complex structural properties by breaking them down into `left_subtree` + `right_subtree` subproblems.
- **Trie**: Eliminates the need to hash entire strings. Validating a prefix takes $O(L)$ time where $L$ is the length of the string, ignoring the millions of other words in the dictionary.

## Progression Guide

### 1. `_must_do` (The Core Mechanics)
- **Level Order Traversal**: The gateway to Tree BFS using slightly modified queues.
- **Zigzag Level Order**: Teaches state-toggling within BFS.
- **Implement Trie**: The classic prefix tree construction.

### 2. `_practice` (Variations)
- **Construct BT from Preorder Inorder**: Testing your fundamental understanding of DFS partitioning.
- **Validate BST**: Using recursive bounds (`-Infinity` to `+Infinity`) to validate structural integrity.
- **Design Add & Search Words**: Combines Trie with Backtracking (DFS) to handle wildcards.

### 3. `_advanced` (Hard Constraints & Combinations)
- **All Nodes Distance K**: Treating a Tree like an undirected Graph by creating parent pointers.
- **Word Search II**: The ultimate combination of Grid Backtracking (DFS) with a Trie!
- **Deepest Leaves Sum & Maximum Width**: Complex BFS/DFS manipulation keeping track of spatial relationships.
