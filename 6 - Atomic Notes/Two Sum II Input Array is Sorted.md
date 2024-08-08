---
id: Two Sum II Input Array is Sorted
aliases: []
tags:
  - twopointer
  - medium
---

# Two Sum II Input Array is Sorted

Given an array of integers `numbers` that is sorted in **non-decreasing order**. 

Return the indices (1-indexed) of two numbers, `[index1, index2]`, such that they add up to a given `target` and `index1<index2`. Note that `index1` and `index2` cannot be equal, therefore you may not use the same element twice. 

THere will always be **exactly one valid solution**.

Your solution must use O(1) additional space. 

### Example 1:
```python 

Input: numbers = [1,2,3,4], target = 3
Output: [1,2]
```
Explaination: 
The sum of 1 and 2 is 3. Since we are assuming a 1-indexed array, `index1 = 1`, `index2 = 2`. We return `[1,2]`

### Constraints: 
```python
- 2 <= numbers.length <= 1000 
- -1000 <= numbers[i] <= 1000 
- -1000 <= target <= 1000
```
### Rough Work/Thought Process: 

Since the array is sorted in ascending order, I think it would be the most proficent to start from the end to get our first pointer and then once we reach a number thats less than the target we then start our second pointer to search the list from our current index for a value which when added to our current value will equal the target. If we don't find another value which adds to this we then decrement the current index of the first pointer. 

### Solution
```python
class Solution:
    def twoSum(self, numbers: List[int], target: int) -> List[int]:
        
        l, r = 0, len(numbers) - 1

        while l < r:
            curSum = numbers[l] + numbers[r]

            if curSum > target:
                r -= 1
            elif curSum < target:
                l += 1
            else:
                return [l + 1, r + 1]
```
Looking at the solution my thought process was pretty wrong because I didn't take advantage of how the list was sorted and overall it was pretty inefficent. 

### Explaination: 
The proper way of solving this with 2 pointers was to have one pointer start at the beginning and the other start at the end and add those to values together, if the sum is less then the target then we would need to increment the pointer on the left and if the sum was greater than the target then we would need to decrement the pointer on the right. Once we get the target we then return them as a tuple after adding 1 to both indexes because we are assuming a 1-indexed array. 


