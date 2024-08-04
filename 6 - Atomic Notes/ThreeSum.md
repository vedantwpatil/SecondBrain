---
id: ThreeSum
aliases:
  - ThreeSum
tags:
  - twopointer
  - medium
---

# ThreeSum

Given an integer array `nums`, return all the triplets `[nums[i], nums[j], nums[k]]` where `nums[i] + nums[j] + nums[k] == 0`, and the indices `i`,`j` and `k` are all distinct. 

The output should not contain any duplicate triplets. You may return the output and the triplets in any order. 

### Example 1: 
```python 

Input: nums = [-1,0,1,2,-1,-4]
Output: [[-1,-1,2],[-1,0,1]]
```

Explaination: 
```python 
nums[0] + nums[1] + nums[2] = (-1) + 0 + 1 = 0.
nums[1] + nums[2] + nums[4] = 0 + 1 + (-1) = 0.
nums[0] + nums[3] + nums[4] = (-1) + 2 + (-1) = 0.
```
The distinct triplets are `[-1,0,1]` and `[-1,-1,2]`

### Example 2: 
```python
Input: nums = [0,1,1]
Output: []
```

Explaination: The only possible triplet does not sum up to 0 

### Example 3: 
```python
Input: nums = [0,0,0]
Output: [[0,0,0]]
```
Explaination: The only possible triplet sums up to 0 

### Constraints: 
```python
- 3 <= nums.length <= 1000 
- 10^5 <= nums[i] <= 10^5
```
### Rough Work/ Thought Process 
 
What we could do is write a triple loop which goes through and all the numbers together and then check to see if they have a target, however this is really inefficent and also allows for the possibility of duplicates although you might be able to remove them by using a [[HashSets|hashset]]. 

Another idea I had was converting the input array into a [[HashSets|hashset]] to be able to get rid of all the duplicates and then go through the list and add the numbers up. However this runs into the same issue where it is still really inefficent. 

### Solution: 
```python
class Solution:
    def threeSum(self, nums: List[int]) -> List[List[int]]:
        res = []
        nums.sort()

        for i, a in enumerate(nums):
            # Skip positive integers
            if a > 0:
                break

            if i > 0 and a == nums[i - 1]:
                continue

            l, r = i + 1, len(nums) - 1
            while l < r:
                threeSum = a + nums[l] + nums[r]
                if threeSum > 0:
                    r -= 1
                elif threeSum < 0:
                    l += 1
                else:
                    res.append([a, nums[l], nums[r]])
                    l += 1
                    r -= 1
                    while nums[l] == nums[l - 1] and l < r:
                        l += 1
                        
        return res
```
