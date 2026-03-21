# Brute Force Approach: Maximum Sum Subarray of Size K

## Intuition
The most straightforward way to find the maximum sum of any contiguous subarray of size $K$ is to calculate the sum of *every possible* subarray of size $K$ and keep track of the maximum sum encountered.

## Approach
1. We iterate through the array with an outer loop variable `i` acting as the starting index of our subarray.
2. The starting index can range from `0` to `N - K` (where $N$ is the array length), because any index after `N - K` won't have $K$ elements remaining to form a valid subarray.
3. For each starting index `i`, we use an inner loop to calculate the sum of the next $K$ elements.
4. We compare this sum with our `max_sum` variable and update `max_sum` if the current sum is larger.

## Complexity Analysis
- **Time Complexity:** $O(N \cdot K)$. For each of the $N-K+1$ subarrays, we are doing a sum of $K$ elements. When $K$ is close to $N$, this degenerates to $O(N^2)$.
- **Space Complexity:** $O(1)$. We only use a few variables (`max_sum`, `current_sum`, `i`, `j`) meaning the space required does not scale with input size.

## Why this leads to Sliding Window
Notice the **overlapping work**.
When calculating the sum of the subarray from index `1` to `K`, it shares exactly $K-1$ elements with the previous subarray (from index `0` to `K-1`).
The only difference is that we lost the element at index `0` and gained the element at index `K`.
Instead of recalculating the entire sum from scratch (which takes $O(K)$ time), we can simply take the previous sum, subtract the element that "slid out" of the window, and add the element that "slid in". This observation reduces the work per subarray from $O(K)$ to $O(1)$, shifting our overall time complexity to $O(N)$.
