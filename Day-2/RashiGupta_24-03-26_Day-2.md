# Day 2 - POTD

## Problem Name:
Remove Duplicates from Sorted Array

## Approach:
- Step 1: Use two pointer approach
- Step 2: Pointer i keeps track of unique elements
- Step 3: Pointer j scans the array
- Step 4: Replace duplicates and return size

## Code:
```cpp
#include <iostream>
using namespace std;

int removeDuplicates(int arr[], int n) {
    if(n == 0) return 0;

    int i = 0;

    for(int j = 1; j < n; j++) {
        if(arr[j] != arr[i]) {
            i++;
            arr[i] = arr[j];
        }
    }

    return i + 1;
}

int main() {
    int arr[] = {1,1,2,2,3};
    int n = 5;

    int k = removeDuplicates(arr, n);

    cout << "Unique elements count: " << k << endl;

    return 0;
}<img width="1904" height="902" alt="Screenshot 2026-03-24 020334" src="https://github.com/user-attachments/assets/8115edef-8c99-4110-98f2-2c531c6c7d6b" />
