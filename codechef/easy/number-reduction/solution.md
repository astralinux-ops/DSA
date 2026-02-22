# Number Reduction

## Problem Information
- **Platform:** Codechef
- **Difficulty:** Easy
- **URL:** https://www.codechef.com/problems/RED23
- **Date:** 2026-02-22

## Solution

```python
# cook your dish here
for i in range(int(input())):
    n = int(input())
    while True:
        if n == 3:
            print(n)
            break
        elif n % 2 == 0:
            n //= 2
        elif n > 3:
            n -= 3
        else:
            print(n)
            break
```

---
*Generated automatically by LeetFeedback Extension*
