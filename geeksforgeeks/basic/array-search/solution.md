# Array Search

## Problem Information
- **Platform:** Geeksforgeeks
- **Difficulty:** Basic
- **URL:** https://www.geeksforgeeks.org/problems/search-an-element-in-an-array-1587115621/1
- **Date:** 2026-02-21

## Solution

```java
class Solution {
    static int search(int arr[], int x) {
        // Iterate through the array using a standard for loop
        // to track the index
        for (int i = 0; i < arr.length; i++) {
            if (arr[i] == x) {
                return i; // Return the first occurrence index
            }
        }
        // If the loop completes without finding x
        return -1;
    }
}
```

---
*Generated automatically by LeetFeedback Extension*
