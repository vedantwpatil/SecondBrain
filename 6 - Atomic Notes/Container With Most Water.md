---
id: Container With Most Water
aliases:
  - Container With Most Water
tags:
  - twopointer
  - medium
---
# Container With Most Water

You are given an integer array `heights` where `heights[i]` represents the height of the i^th bar. 

You may choose any two bars to form a container. Return the *maximum* amount of water a container can store. 

### Example 1: 
```python
Input: height = [1,7,2,5,4,7,3,6]
Output: 36
```

### Example 2: 
```python
Input: height = [2,2,2]
Output: 4
```
### Constraints:
- 2 <= `height.length` <= 1000
- 0 <= `height[i]` <= 1000 

### Rough Work/Thought Process:

This section got lost and deleted when I lost access to all my files. 

### Solution
```python
class Solution():
  def containerWithMostWater(self, height :List[ints]) ->:
    left, right = 0, len(height) - 1 
    sum = 0 

    while left < right: 
      sum = max(sum, min(height[left], height[right]) * (right - left))
      if heights[left] < heights[r]:
        left += 1 
      if heights[left] >= heights[right]:
        right -= 1

    return sum

```
### Explanation:
So what we are doing is trying to find the biggest rectangle we can with the height of the rectangle being determined by the smaller height amongst the two pillars and the width being represented by how far the indexes of the two pillars are apart.

So what we are doing in our code is initializing our pointers at the start and the end of the input array, this is so we can have the biggest width possible. After this we then start our loop which inside of it we will calculate the biggest container we can make at the current index following all the conditions. We calculate the min of the two heights because that's one of the conditions so that is our length and we calculate the width by subtracting the distance between our pointers. 

After this we then increment or decrement our pointers depending on which one is bigger than the other. 

