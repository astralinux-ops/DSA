# Zigzag Conversion

## Problem Information
- **Platform:** Leetcode
- **Difficulty:** Medium
- **URL:** https://leetcode.com/problems/zigzag-conversion/submissions/1926775041/
- **Date:** 2026-02-21

## Solution

```text
func convert(s string, numRows int) string {
    // Edge case: if rows are 1 or string is shorter than rows, return as is
    if numRows == 1 || numRows >= len(s) {
        return s
    }

    // Create a slice of byte slices to represent each row
    rows := make([][]byte, numRows)
    currentRow := 0
    goingDown := false

    for i := 0; i < len(s); i++ {
        // Append current character to the current row
        rows[currentRow] = append(rows[currentRow], s[i])

        // Reverse direction if we hit the top or bottom
        if currentRow == 0 || currentRow == numRows-1 {
            goingDown = !goingDown
        }

        // Move to the next row
        if goingDown {
            currentRow++
        } else {
            currentRow--
        }
    }

    // Combine all rows into a single result
    result := make([]byte, 0, len(s))
    for _, row := range rows {
        result = append(result, row...)
    }

    return string(result)
}
```

---
*Generated automatically by LeetFeedback Extension*
