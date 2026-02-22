# Decrement OR Increment

## Problem Information
- **Platform:** Codechef
- **Difficulty:** Easy
- **URL:** https://www.codechef.com/problems/DECINC
- **Date:** 2026-02-22

## Solution

```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n;
    cin >> n;
    if (n % 4 == 0) n++;
    else n--;
    cout << n << endl;
    return 0;
}
```

---
*Generated automatically by LeetFeedback Extension*
