# Room Allocation

## Problem Information
- **Platform:** Codechef
- **Difficulty:** Easy
- **URL:** https://www.codechef.com/problems/ROOMALLOC
- **Date:** 2026-02-22

## Solution

```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    // your code goes here
    int t;
    cin >> t;
    while(t--){
        int n, s = 0;
        cin >> n;
        int a[n];
        for(int i = 0; i < n; i++){
            cin >> a[i];
            s += a[i] / 2 + a[i] % 2;
        }
        cout << s << endl;
    }

}

```

---
*Generated automatically by LeetFeedback Extension*
