---
id: Contains Duplicate
aliases: []
tags:
  - hashing
  - easy
  - array
---

# Contains Duplicate

Given an integer array `nums`, return `true` if any value appears at least twice in the array, and return false if every element is distinct

#### Example 1:
	Input: nums = [1,2,3,1]
	Output: true
#### Example 2:
	Input: nums = [1,2,3,4]
	Output: true
#### Example 3: 
	Input: nums = [1,1,1,3,34,3,2,4,2]
	Output: true

Constraints:
- $1 \leq$ `nums.length` $\leq 10^5$
- $-10^9 \leq$ `nums[i]` $\leq 10^9$


```python
class Solution(object):
	def containsDuplicate(self,nums):
	"""
	:type nums: List[int]
	:rtype: bool
	"""
	num_set = set()
	for num in nums: 
		if num in num_set:
			return True
		num_set.add(num)
	return False
	
```

The reason this code works is that the data structure a set will never contain duplicate values. So we automatically assume that every element is distinct and return false and check for if the next element we are adding is already in the set, if it is we return true that there is a duplicate. If not then we continue on adding elements in the list. 
