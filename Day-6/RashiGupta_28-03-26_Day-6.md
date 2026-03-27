# Day 6 - POTD

## Problem Name:
Check If N and Its Double Exist 

## Approach:
- Step 1: Use a set to store visited elements
- Step 2: Traverse the array
- Step 3: For each element x:
    - Check if 2*x exists in set
    - OR if x is even, check if x/2 exists in set
- Step 4: If found, return true
- Step 5: Otherwise, insert x into set
- Step 6: If no pair found, return false

## Code:
```cpp
#include <iostream>
#include <vector>
using namespace std;

int main() {
    bool checkIfExist(vector<int>& arr) {
        int n=arr.size();
        for(int i=0; i<n; i++){
            for(int j=i; j<n; j++){
                if(i!=j && (arr[i]==2*arr[j] || arr[j]==2*arr[i])){
                    return true;
                }
            }
        }
        return false;
    }

    return 0;
}
