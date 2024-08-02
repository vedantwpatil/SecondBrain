---
id: Longest Consecutive Sequence
aliases: []
tags: []
---

2024-07-02 16:19

Status: 

Tags: #array #hashing

# Longest Consecutive Sequence

Given an array of integers `nums`, return the length of the longest consecutive sequence of elements,

A consecutive sequence is a sequence of elements in which each element is exactly `1` greater than the previous element. 

You must write an algorithm that runs in 0(n) times. 

### Example 1: 
```python 
Input: nums = [2,20,4,10,3,4,5]
Output: 4
```

Explaination: The longest consecutive sequence is `[2, 3, 4, 5]`.

### Example 2: 
```python

Input: nums = [0,3,2,5,4,6,1,1]
Output: 7
```

### Constraints: 
- `0 <= nums.length <= 1000`
- `-10^9 <= nums[i] <= 10^9`

### Thought Process/Rough Work:

At first thought I wanted to add all the elements to a hashset and see the longest consecutive sequence however it doesn't insert in order as well as I don't think that this would be fast enough to be in O(n) time. 

My next thought process was thinking of using the [[Bucket Sort]] algorithm, I then searched up the solution and found that what we can do is take each value and check if the value that preceeds it is present in the set, if it is not then we know that this is the start of a sequence and can then check how many consecutive numbers are present in the array. If it is not the start of a sequence we don't make a sequence yet. 

### Solution:

```python
class Solution:
    def longestConsecutive(self, nums: List[int]) -> int:
        numSet = set(nums)
        longest = 0 

        for n in nums: 
            if (n-1) not in numSet:
                length = 0 
                while (n + length) in numSet:
                    length += 1 
                longest = max(length, longest)

        return longest 

```

### Explaination:

After visualizing the problem we can realize how to create sequences and then evaluate the longest sequence. We checked to see if the current value had a preceeding value and if it doesnt we know that it is the start of a sequence, we then keep checking if there are proceeding values in our array by adding the start of the sequence to the length. We then get the biggest value out of the length of that current sequence and compare it to the longest sequence we've found. 

