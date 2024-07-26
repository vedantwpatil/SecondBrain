---
id: Top K Frequent Elements
aliases: []
tags: []
---

2024-07-02 16:20

Status: 

Tags: #array #hashing 

# Top K Frequent Elements

Given an integer array `nums` and an integer `k`, return the *`k` most frequent elements*. You may return the answer in **any order**.

### Example 1:

`Input: nums = [1,2,2,3,3,3], k = 2`
`Output: [2,3]`

### Example 2: 

`Input: nums = [7,7], k = 1`
`Output: [7]`

### Constraints: 
`1 <= nums.length <= 10^4`
`-1000 <= nums[i] <= 1000`
`1 <= k <= number of distinct elements in nums.`

### Rough Work/Thought Process 

Since we need to return the most k frequent amount of elements we should first count the amount of numbers each of the arrays have and return the length of the 2 largest arrays. The way we would do this is by creating a hashmap with the keys being the number of the element and then returning the lists of the 2 longest keys. 

### Solution 

This problem uses the algorithm called [[Bucket Sort]] which allows this problem to be solved in linear time 
Time Complexity: O(n)
```python
class Solution(object):
    def topKFrequent(self, nums, k):
        """
        :type nums: List[int]
        :type k: int
        :rtype: List[int]
        """

        count = {}
        freq = [[] for i in range(len(nums) + 1)]

        for n in nums:
            count[n] = 1 + count.get(n, 0)
        for n, c in count.items():
            freq[c].append(n)

        res = []
        for i in range(len(freq) - 1, 0, -1):
            for n in freq[i]:
                res.append(n)
                if len(res) == k:
                    return res
```
### Explaination: 
We create a array with the index for each element being the amount of times the element has been in the phrase. We then need to return the array, while making the array we create it to be the length of our original array because you can't have more than elements than the length of the phrase. We then start at the end of the array and append the values into the array. While doing this we check to see if our new array is the size of `k` because we want the `k` most frequent elements. 
