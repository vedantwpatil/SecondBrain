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
        
### Solution 

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
# Reference
