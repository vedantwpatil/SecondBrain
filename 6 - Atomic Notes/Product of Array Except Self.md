---
id: Product of Array Except Self
aliases: []
tags: []
---

# Product of Array Except Self

Given an integer array `nums`, return an array `output` where `output[i]` is the product of all elements of `nums` except `nums[i]`. Each product is **guaranteed** to fit in a **32-bit** integer 

Follow-up: Could you solve it in O(n) time without using the division operation?

### Example 1: 

```python 
Input: nums = [1,2,4,6]
Output: [48,24,12,8]
```
### Example 2: 

```python 
Input: nums = [-1,0,1,2,3]
Output: [0,-6,0,0,0]
```
### Constraints: 

- 2 <= `nums.length` <= 1000
- 20 <= `nums[i]` <= 20

### Thought Process/Rough Work:
The problem would be really easy if we were able to either do it in a slower time than O(n) or if we were allowed to do it using the division operation because we could multiple all the elements by each other and divide the value by the value at the current index. Likewise it would be easy if we didn't need the solution to be faster than O(n) because we could just loop through the array twice and calculate the value we need and insert it at the index we need it to be at. 

We use a strategy called prefix and postfix to solve these questions, to do this we calculate the value of the numbers going both left to right and right to left and multiply them by the prefix and postfix values. We update our prefix and postfix values after multiplying the intial value by the value in the input array and then storing that value in the array by doing this we will get the values of all the elements besides the element at the current index

### Solution:
Time Complexity: O(n)
Space Complexity: O(n)

```python 
class Solution:  
    def productExceptSelf(self, nums: List[int]) -> List[int]:
        result = [1] * (len(nums))

        prefix = 1 
        for i in range(len(nums)):
            result[i] = prefix
            prefix *= nums[i]

        postfix = 1 
        for i in range(len(nums) -1, -1, -1):
            result[i] *= postfix
            postfix *= nums[i]
        return result
```

### Explanation: 
We use our prefix and postfix strategy to calculate the numbers we need, to do this we need 2 separate for loops, one to calculate the prefix and the other to calculate the postfix. While we are looping through, for prefix we need to store the prefix elements into the array while updating the prefix by multiplying the elements by the prefix. For postfix we need to loop from the back and to calculate the result we need to multiply our values by the postfix and then update the postfix after by multiplying it by the element at the current index in the input array. After this our final array will hold all the required elements we need. 
