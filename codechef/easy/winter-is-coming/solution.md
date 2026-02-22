# Winter is Coming

## Problem Information
- **Platform:** Codechef
- **Difficulty:** Easy
- **URL:** https://www.codechef.com/problems/LMP2E
- **Date:** 2026-02-22

## Solution

```python
t = int(input())

for _ in range(t):
    n, A, B = map(int, input().split())
    temps = list(map(int, input().split()))
    
    wearing = False  # Chef starts without a jacket
    count = 0
    
    for temp in temps:
        if temp < A:
            if not wearing:
                count += 1
                wearing = True
        elif temp > B:
            if wearing:
                wearing = False
    
    print(count) 
```

---
*Generated automatically by LeetFeedback Extension*
