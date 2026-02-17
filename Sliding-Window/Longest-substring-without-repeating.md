Longest Substring Without Repeating Characters
Core Constraint
At every step the current window must contain only unique characters.
The algorithm is not searching substrings — it is maintaining a valid state while scanning a stream.

Why Brute Force Fails
Checking every substring requires restarting the search whenever a duplicate appears.
This repeatedly recomputes information we already know, leading to O(N²) time.
The inefficiency comes from discarding useful state.

Key Invariant
The window [left, right] always contains unique characters.
Instead of rebuilding the window, we shrink it only until the constraint becomes valid again.
We never move left backward → total movements are linear.

Reasoning
We treat the string as a stream of tokens.
When a new character arrives:
If unseen → expand window
If seen → move left pointer to just after its previous occurrence
The window dynamically adapts rather than restarting.
This transforms a quadratic search into constraint maintenance.

Complexity
Time: O(N)
Space: O(K) where K is character set size

Transferable Insight (Deep Learning)
This problem is equivalent to maintaining a limited context memory.
The sliding window behaves like a bounded attention span:
the model keeps recent relevant tokens and discards conflicting ones.
Transformers do something similar — context is not recomputed from scratch,
it is updated incrementally while preserving constraints.

The algorithm teaches:
Efficient learning systems maintain valid state instead of recomputing history.
Implementation (Python)
def lengthOfLongestSubstring(s: str) -> int:
    last = {}
    left = 0
    ans = 0

    for right, ch in enumerate(s):
        if ch in last and last[ch] >= left:
            left = last[ch] + 1

        last[ch] = right
        ans = max(ans, right - left + 1)

    return ans
