---
id: Best Time to Buy and Sell Stock
aliases:
  - Best Time to Buy and Sell Stock
tags:
  - easy
  - slidingwindow
  - twopointer
---

# Best Time to Buy and Sell Stock

You are given an integer array `prices` where `prices[i]` is the price of NeetCoin on the `ith` day. 

You may choose **single day** to buy one NeetCoin and choose a **different day in the future** to sell it. 

Return the maximum profit you can achieve. You may choose to **not make any transactions**, in which case the profit would be `0`. 

### Example 1: 
```python
Input: prices = [10,1,5,6,7,1]
Output: 6
```

Explanation: Buy `prices[i]` and sell `prices[4], profit = 7 - 1 = 6`.

### Example 2:
```python

Input: prices = [10,8,7,5,2]
Output: 0
```
Explanation: No profitable transactions can be made, thus the max profit is 0.

### Constraints:
```python
- 1 <= prices.length <= 100
- 0 <= prices[i] <= 100 
```
### Rough Work/Thought Process 

While trying to solve this question, it would be convenient if we could get the best profit by searching the list for the maximum value and minimum value and selling/buying on those days but time is constantly flowing so we need to be searching the list from left to right. 

We would use some type of two pointer solution where our left pointer is the day we buy and the right pointer is the day we sell. 

If we check to see the profit we can get, if we have positive profit, we will keep our buying pointer were it is and if we get negative profit we will move our left pointer to the current index. We keep track of our profit and if there ever is a greater value we can update our selling pointer to be that one. 

### Solution:
```python
class Solution(object):
  def maxProfit(self, prices :List[int]) -> int: 
    left, right = 0 
    max_profit = 0

    while right < len(prices):
      if prices[left] < prices[right]: 
        profit = prices[right] - prices[left] 
        max_profit = max(max_profit, profit)

      else:
        left = r
      right += 1

  return max_profit
```
### Explanation
While searching for the maximum profit we use two pointers, one will be our selling price the other will be our buying price. We want our buying price to be lower than our selling price but we also want to maximize profit. So while going through this list if we ever see that our buying price is higher than our selling price, we will change our buying price to that new index. We then calculate the profit we get from that and if we get a profit bigger than any of our previous profits we now want to set that as our new max profit. 

