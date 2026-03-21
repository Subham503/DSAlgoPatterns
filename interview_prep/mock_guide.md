# Mock Interview Guide

To graduate from Tier 3 to Tier 4, you must be able to perform under pressure. This guide defines how to conduct a 45-minute peer mock interview using the patterns in this repository.

## The 45-Minute Breakdown

| Time | Phase | Interviewer Action | Interviewee Action |
| :--- | :--- | :--- | :--- |
| **0-5m** | **Introduction & Problem Statement** | Paste the `.md` problem description without the solution block. | Read aloud, clarify constraints (e.g., "Can the array be negative?", "Is it sorted?"). |
| **5-15m** | **Brute Force & Pattern Recognition** | Wait. Nudge only if they are completely stuck. | Verbally explain the naive $O(N^2)$ or $O(2^N)$ approach. Identify the problem signals that map to a pattern in the `PATTERN_CATALOG.md`. |
| **15-20m** | **Algorithm Design** | Ask "What is the time complexity of that?" | Propose the optimal pattern (e.g., "This requires a Variable Sliding Window"). Map out the variables needed (`left`, `right`, `max_len`). |
| **20-35m** | **Implementation** | Watch for off-by-one errors and edge cases. | Write the code. Think out loud line-by-line. Do not go silent for more than 30 seconds. |
| **35-42m** | **Dry Run & Testing** | Provide a tricky edge case. | Dry-run the code manually with a small test case. Find your own bugs before the compiler does. |
| **42-45m** | **Feedback** | Use the rubric below to score. | Listen and take notes on `PROGRESS.md`. |

## Evaluation Rubric (1-5 Scale)
1. **Communication:** Did they think out loud? Did they explain the *why* before the *how*?
2. **Problem Solving:** Did they correctly identify the pattern? Did they jump straight to coding or plan first?
3. **Coding Speed & Accuracy:** Was the code clean, modular, and mostly bug-free on the first run?
4. **Testing:** Did they independently verify their logic with a dry run?

## Next Steps
Use the `practice_sets/` folder to select a curated group of 3 problems for your next session.
