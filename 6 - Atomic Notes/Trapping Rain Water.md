---
id: Trapping Rain Water
aliases: []
tags:
  - twopointer
  - hard
---

# Trapping Rain Water

You are given an array non-negative integers `heights` which represent an elevation map. Each value `heights[i]` represents the height of a bar, which has a width of `1`. 

Return the maximum area of water that can be trapped between the bars.

### Example 1:
```python
Input: height = [0,2,0,3,1,0,1,3,2,1]
Output: 9
```
### Constraints: 
- 1 <= `height.length` <= 1000
- 0 <= `height[i]` <= 1000

### Rough Work/Thought Process:
I think this problem is really hard as you can't easily tell where the start and end of the container is and where the start and the end is for the water. 

I am thinking that since our input array gives us an array of heights, we start our first pointer and then start our second pointer until we find something which is either taller or smaller than our current height, then we can calculate how much water is being held by calculating the min height.

That solution wont work though because it assumes that everything is going to be in the perfect square shape. 

Something which is common is that out of the two pillars, we have to take the height of the minimum as otherwise we are unable to capture enough water. So this is apart of our calculation for how much water there is. 

If we calculate the max height on the left and the right of each of the pillars, we then can compare the minimum of that to the current value to evaluate how much water can be stored. 

### Solution: 
```python
class Solution(object):
  def trappingRainWater(heights:List[int]):
    left, right = 0, len(heights) - 1 

    if not height:
      return 0
    
    leftMax, rightMax = height[left], height[right]
    result = 0 
    while left < right: 
      if leftMax < rightMax:
        left += 1 
        leftMax = max(leftMax, height[left])
        res += leftMax - height[left]
      else: 
        r -= 1 
        rightMax = max(rightMax, height[right])
        res += rightMax - height[right]

    return result 
```
### Explanation: 

Using two pointers we are able to be a lot more efficient by calculating the maximum value the pillar can be we can figure out the max potential value of the water. With this we can then compare this against the height of the current index and depending on that determines how much water we are able to store. 
