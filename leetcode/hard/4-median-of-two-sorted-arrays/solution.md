# Median of Two Sorted Arrays

## Problem Information
- **Platform:** Leetcode
- **Difficulty:** Hard
- **URL:** https://leetcode.com/problems/median-of-two-sorted-arrays/submissions/1926546627/
- **Date:** 2026-02-21

## Solution

```python
class Solution(object):
    def findMedianSortedArrays(self, nums1, nums2):
        # Ensure nums1 is the smaller array to optimize binary search complexity
        if len(nums1) > len(nums2):
            nums1, nums2 = nums2, nums1
        
        m, n = len(nums1), len(nums2)
        low, high = 0, m
        
        while low <= high:
            partitionX = (low + high) // 2
            # Total elements on left = (m + n + 1) // 2
            partitionY = (m + n + 1) // 2 - partitionX
            
            # Edge cases: handle partitions at the very beginning or end
            maxLeftX = nums1[partitionX - 1] if partitionX > 0 else float('-inf')
            minRightX = nums1[partitionX] if partitionX < m else float('inf')
            
            maxLeftY = nums2[partitionY - 1] if partitionY > 0 else float('-inf')
            minRightY = nums2[partitionY] if partitionY < n else float('inf')
            
            # Check if we found the correct partition
            if maxLeftX <= minRightY and maxLeftY <= minRightX:
                # If total elements are even
                if (m + n) % 2 == 0:
                    return (max(maxLeftX, maxLeftY) + min(minRightX, minRightY)) / 2.0
                # If total elements are odd
                else:
                    return float(max(maxLeftX, maxLeftY))
            
            # If we are too far right in nums1, move left
            elif maxLeftX > minRightY:
                high = partitionX - 1
            # If we are too far left in nums1, move right
            else:
                low = partitionX + 1
```

---
*Generated automatically by LeetFeedback Extension*
