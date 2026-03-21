# Brute Force Approach: Longest Substring Without Repeating Characters

## Intuition
To find the longest substring without repeating characters, we can generate all possible substrings, check each one to see if it contains any duplicate characters, and keep track of the maximum length among those that don't.

## Approach
1. Use an outer loop `i` to fix the starting index of the substring.
2. Use an inner loop `j` starting from `i` to fix the ending index of the substring. The substring is from `s[i...j]`.
3. For each substring generated, use a nested loop (or a hash set) to check if all characters in the substring `s[i...j]` are unique.
4. If they are unique, we update `max_length = max(max_length, j - i + 1)`.

## Complexity Analysis
- **Time Complexity:** $O(N^3)$. There are $O(N^2)$ possible substrings. For each substring of length $L$, checking for uniqueness takes $O(L)$ time. Summing this up leads to $O(N^3)$. Note: You can optimize the uniqueness check to $O(1)$ by incrementally adding to a set as `j` moves, which brings it down to $O(N^2)$, but it's still slow for large strings.
- **Space Complexity:** $O(min(N, M))$ where $M$ is the size of the charset (e.g., 26 for English letters). We need a set to keep track of the characters seen in the current substring.

## Why this leads to Sliding Window
Notice the **redundant checks**. 
If we know that the substring `s[i...j]` has no repeating characters, and we expand to `s[i...j+1]` which introduces a duplicate, we know that *any* substring starting at `i` and ending *after* `j+1` will also contain that duplicate. 
Therefore, instead of restarting from `i+1` and checking everything again, we can just use a "window" `[left, right]`. We expand `right` until we hit a duplicate, and then we shrink `left` just enough to remove the duplicate character from our window. This reduces the time complexity to $O(N)$ since both `left` and `right` only traverse the string once.
