# Masterchef finals

## Problem Information
- **Platform:** Codechef
- **Difficulty:** Basic
- **URL:** https://www.codechef.com/problems/TOP10
- **Date:** 2026-02-21

## Solution

```cpp
using namespace std;

int main() {
    int T;
    // Read the number of test cases
    cin >> T;

    while (T--) {
        int X;
        // Read Chef's current rank
        cin >> X;

        // Chef makes it if his rank is 10 or better (1, 2, ..., 10)
        if (X <= 10) {
            cout << "YES" << endl;
        } else {
            cout << "NO" << endl;
        }
    }
    return 0;
}
```

---
*Generated automatically by LeetFeedback Extension*
