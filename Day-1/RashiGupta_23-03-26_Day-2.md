
# Day 2 - POTD

## Problem Name:
TWO SUM

## Approach:
- Step 1: Traverse the array elements through i index
- Step 2: Second index j also traverse after i and do compare sum with the target
- Step 3: Returns index values if summation=target.

## Code:
```cpp
#include <iostream>
using namespace std;

int main() {
    // your code here

      vector<int> twoSum(vector<int>& nums, int target) {
        int n=nums.size();
        vector<int> v;
        for(int i=0; i<n; i++){
            for(int j=i+1; j<n; j++){

                if(nums[i]+nums[j]==target){
                    return {i,j};
                }
            }
        }
        return {};
    }   
}

//Time complexity: O(n2)
//Space complexity: O(1).
