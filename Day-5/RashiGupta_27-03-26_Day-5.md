# Day 5 - POTD

## Problem Name:
Move Zeroes 

## Approach:
- Step 1: Use two pointers (i, j)
- Step 2: Pointer j tracks position to place non-zero element
- Step 3: Traverse array using i
- Step 4: If nums[i] != 0, swap nums[i] and nums[j]
- Step 5: Increment j
- Step 6: Continue until end



## Code:
```cpp
#include <iostream>
using namespace std;

void main(){
class Solution {
public:
    void moveZeroes(vector<int>& nums) {
        int j=0;
        int n=nums.size();
        for(int i=0; i<n; i++){
            if(nums[i]!=0){
               swap(nums[i],nums[j]);
               j++;
            }
        }
    }
};
}
