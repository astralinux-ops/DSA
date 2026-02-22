# Valentine Gifts

## Problem Information
- **Platform:** Codechef
- **Difficulty:** Easy
- **URL:** https://www.codechef.com/problems/VAL142
- **Date:** 2026-02-22

## Solution

```python
def can_plan_gifts(budget):
    # Calculate the total cost of gifts for all 7 days using the formula for the sum of a geometric series
    total_cost = (2 ** 7 - 1)  # 2^7 - 1 is the sum of a geometric series with 7 terms
    
    if total_cost <= budget:
        return "YES"
    else:
        return "NO"


# Input
t = int(input().strip())

for _ in range(t):
    x = int(input().strip())
    result = can_plan_gifts(x)
    print(result)

```

---
*Generated automatically by LeetFeedback Extension*
