---
id: Two Sum
aliases: []
tags:
  - easy
  - hashing
  - array
---

# Two Sum

Given an array of integers `nums` and an integer `target`, return the number indices `i` and `j` such that `nums[i] + nums[j] == target` and `i != j`. 

You may assume that *every* input has exactly one pair of indices `i` and `j` that satisfy the condition. 

Return the answer with the smaller index first. 

### Example 1: 

```python
Input:
nums = [3,4,5,6], target = 7

Output: [0,1]
```

Explanation: `nums[0] + nums[1] == 7` so we return `[0,1]`

### Example 2:
```python
Input: nums = [4,5,6], target = 10

Output: [0,2]
```
### Example 3: 
```python
Input: nums = [5,5], target = 10

Output: [0,1]
```

### Constraints:
- 2 <= `nums.length` <= 1000
- `-10,000,000 <= nums[i] <= 10,000,000`
- `-10,000,000 <= target <= 10,000,000`

#### Solution:
``` python
class Solution(object):
	def twoSum(self, nums, target):
		"""
		:type nums: List[int]
		:type target: int 
		:rtype List[int]
		"""
		for i in range(len(nums)):
			for j in range(i + 1, len(nums)):
				if(i != j and nums[i]+nums[j == target]):
					return [i,j]
		return []
```

#### Explanation:
We need to go through the list of integers and find the indexes of the 2 elements which add up to the target value. We can do this by starting a loop through the list and starting a secondary loop which starts at the current index of the former loop while going to the end of the list. Then we just need to check if the indexes are not the same value and if the values at those indexes equal the target. If they do then we need to return those as the correct values as a list. If not then we return an empty list.


