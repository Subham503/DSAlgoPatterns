# Pattern Catalog: The Heuristics Table

The most common question in coding interviews isn't "how do I code this?" but "**how do I know which pattern to use?**"

This catalog provides the heuristics—the signals in the problem description—that tell you exactly which pattern to apply.

## The Heuristics Decision Matrix

| Problem Signal | Likely Pattern | Why & Example |
| :--- | :--- | :--- |
| **Array + Subarray + Sum/K** | **Sliding Window / Prefix Sum** | Need to consider contiguous elements. If K fixed → Fixed SW. If K variable → Variable SW or Prefix Sum + Hash. |
| **String + Permutation + Order** | **Sliding Window (Character Frequency)** | Problem mentions "anagram," "rearrange," or "substring containing all characters." |
| **Array + Sorted + Find Pair/Triplet** | **Two Pointers (Collision)** | If array is sorted, two pointers from ends is often the most efficient way to find a pair. Example: Two Sum II, 3Sum. |
| **Array + Find Cycle / Duplicate** | **Fast & Slow Pointers / Floyd's Cycle** | Linked lists or arrays where values are indices (find duplicate) are classic cycle detection. Example: Find the Duplicate Number. |
| **Graph + Shortest Path + Unweighted** | **BFS (Breadth-First Search)** | BFS explores uniformly outwards, guaranteeing the shortest path in an unweighted graph. Example: Word Ladder. |
| **Graph + Shortest Path + Weighted** | **Dijkstra’s Algorithm** | If weights are positive and you need the minimum distance. Example: Network Delay Time. |
| **Optimal Value + Decision + Search Space** | **Binary Search on Answer** | Problem asks for "maximum minimum" or "minimum maximum." You can decide if a candidate answer is feasible in O(N). Example: Koko Eating Bananas. |
| **Tree + Level-by-Level Traversal** | **Tree BFS** | When you need to process nodes depth by depth. Example: Binary Tree Right Side View. |
| **Tree + Path from Root to Leaf** | **Tree DFS / Backtracking** | When you need to explore every complete path. Example: Path Sum II. |
| **Maximize/Minimize + Overlapping Subproblems**| **Dynamic Programming** | If you can break the problem into smaller identical problems and cache the results. Example: Longest Common Subsequence. |
| **Kth Smallest/Largest + Stream/Unsorted** | **Heap / Priority Queue** | When you need to maintain a running top K elements. Example: K Closest Points to Origin. |
| **String + Prefix Matching / Dictionary** | **Trie (Prefix Tree)** | When you need to rapidly search for word prefixes or autocomplete. Example: Implement Trie. |

---

### How to use this catalog
When faced with a new problem, don't start coding immediately.
1. Identify the input data structure (Array, String, Graph, Tree).
2. Identify the goal (Find a pair, Shortest Path, Kth largest).
3. Cross-reference with the left column of this table to find your optimal pattern.
