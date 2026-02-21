# Longest Palindromic Substring

## Problem Information
- **Platform:** Leetcode
- **Difficulty:** Medium
- **URL:** https://leetcode.com/problems/longest-palindromic-substring/submissions/1926610757/
- **Date:** 2026-02-21

## Solution

```python
class Solution(object):
    def longestPalindrome(self, s):
        if not s or len(s) < 1:
            return ""
        
        start, end = 0, 0
        
        for i in range(len(s)):
            # Check for odd-length palindromes (center is at i)
            len1 = self.expandAroundCenter(s, i, i)
            # Check for even-length palindromes (center is between i and i+1)
            len2 = self.expandAroundCenter(s, i, i + 1)
            
            # Take the maximum length found at this center
            max_len = max(len1, len2)
            
            # If we found a longer palindrome, update our boundaries
            if max_len > end - start:
                # Calculation to find start/end from center i and total length
                start = i - (max_len - 1) // 2
                end = i + max_len // 2
                
        return s[start:end + 1]

    def expandAroundCenter(self, s, left, right):
        L, R = left, right
        # Expand as long as pointers are in bounds and characters match
        while L >= 0 and R < len(s) and s[L] == s[R]:
            L -= 1
            R += 1
        # Return the length of the palindrome found
        # (R - L - 1) because the loop stops after L/R move one step too far
        return R - L - 1
```

---
*Generated automatically by LeetFeedback Extension*
