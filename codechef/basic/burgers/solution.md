# Burgers

## Problem Information
- **Platform:** Codechef
- **Difficulty:** Basic
- **URL:** https://www.codechef.com/problems/BURGERS
- **Date:** 2026-02-22

## Solution

```cpp
using namespace std;

int main() {
    // your code goes here
    int t,a,b,c;
    cin >>t;
    while(t--)
    {
        cin >>a >>b;
        if(a>b)
        c=b;
        else if(a<b)
        c=a;
        else 
        c=b;
        cout<<c;
        cout<<"\n";
    }
    return 0;
}

```

---
*Generated automatically by LeetFeedback Extension*
