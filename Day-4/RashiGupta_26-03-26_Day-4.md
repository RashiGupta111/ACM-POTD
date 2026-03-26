# Day 4 - POTD

## Problem Name:
Best Time to Buy and Sell Stock (LeetCode)

## Problem Statement:
You are given an array prices where prices[i] is the price of a given stock on the ith day.

You want to maximize your profit by choosing a single day to buy one stock and choosing a different day in the future to sell that stock.

Return the maximum profit you can achieve. If no profit is possible, return 0.

## Approach:
- Step 1: Initialize minimum price as first element
- Step 2: Traverse the array
- Step 3: At each step, calculate profit = current price - minimum price
- Step 4: Update maximum profit
- Step 5: Update minimum price if current price is smaller

## Code:
```cpp
#include <iostream>
using namespace std;

int maxProfit(int prices[], int n) {
    int minPrice = prices[0];
    int maxProfit = 0;

    for(int i = 1; i < n; i++) {
        if(prices[i] < minPrice) {
            minPrice = prices[i];
        }
        else {
            int profit = prices[i] - minPrice;
            if(profit > maxProfit) {
                maxProfit = profit;
            }
        }
    }

    return maxProfit;
}

int main() {
    int prices[] = {7,1,5,3,6,4};
    int n = 6;

    cout << "Maximum Profit: " << maxProfit(prices, n) << endl;

    return 0;
}
