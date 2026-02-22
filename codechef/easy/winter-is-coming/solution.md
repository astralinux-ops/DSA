# Winter is Coming

## Problem Information
- **Platform:** Codechef
- **Difficulty:** Easy
- **URL:** https://www.codechef.com/problems/LMP2E
- **Date:** 2026-02-22

## Solution

```cpp
     int c=0;
     int arr[n];
     for(int i=0; i<n; i++){
         cin>>arr[i];
     }
     bool x=false;
     for(int i=0; i<n; i++){
          if(arr[i]<a){
              if(!x){
                  x=true;
                  c++;
              }
         }
         else if(arr[i]>b){
             x=false;
         }
     }
     cout<<c<<endl;
 }
}

```

---
*Generated automatically by LeetFeedback Extension*
