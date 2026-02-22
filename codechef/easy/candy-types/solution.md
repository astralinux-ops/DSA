# Candy Types

## Problem Information
- **Platform:** Codechef
- **Difficulty:** Easy
- **URL:** https://www.codechef.com/problems/CANDYTYPE
- **Date:** 2026-02-22

## Solution

```python
# cook your dish here
from collections import Counter
t = int(input())
for _ in range(t):
    n = int(input())
    arr = list(map(int,input().split()))
    freq = Counter(arr)
    g = Counter(arr).values()
    k = max(g)
    r = []
    for i,j in freq.items():
        if j==k:
            r.append(i)
    r.sort()
    print(r[0])
```

---
*Generated automatically by LeetFeedback Extension*
