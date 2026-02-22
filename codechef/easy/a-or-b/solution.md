# A or B

## Problem Information
- **Platform:** Codechef
- **Difficulty:** Easy
- **URL:** https://www.codechef.com/problems/AORB
- **Date:** 2026-02-22

## Solution

```cpp
#include <iostream>
using namespace std;
int main() {
    int t; cin >> t;
    while(t--) {
        int x, y; cin >> x >> y;
        int ab = (500 - 2*x) + (1000 - 4*(x+y));
        int ba = (1000 - 4*y) + (500 - 2*(y+x));
        cout << max(ab, ba) << endl;
    }
    return 0;
}
```

---
*Generated automatically by LeetFeedback Extension*
