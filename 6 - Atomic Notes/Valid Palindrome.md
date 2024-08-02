---
id: Valid Palindrome
aliases: []
tags: []
---

# Valid Palindrome 
Given a string `s`, return `true` if is a **palindrome**, otherwise return `false`

A palindrome is a string that reads the same forward and backward. It is also case-insensitive and ignores all non-alphanumeric characters. 

### Example 1: 
```python
Input: s = "Was it a car or a cat I saw?"
Output: true
```
Explaination: After considering only alphanumerical characters we have "wasitacaroracatisaw" which is a palindrome 

### Example 2: 
```python
Input: s = "tab a cat"
Output: false
```
Explaination: "tabcat" is not a palindrome 

### Constraints: 
- `1 <= s.length <= 1000`
- `s` is made up of only printable ASCII characters

### Rough Work/Thought Process
In order to check for the word being a palindrome we should use 2 seperate pointers to check the first and last letter to see if they align, by default we assume that the word is a palindrome and check to see if it is false. 

### Solution:
```python
class Solution:
    def isPalindrome(self, s: str) -> bool:
        # Convert to lowercase and remove non-alphanumeric characters
        s = ''.join(char.lower() for char in s if char.isalnum())
        
        # Compare characters from both ends
        left, right = 0, len(s) - 1
        while left < right:
            if s[left] != s[right]:
                return False
            left += 1
            right -= 1
        
        return True
```

### Explaination: 
We first need to change all the characters to the same case and remove all the non-alphanumeric characters. After this we then compare the two pointers to see if they have the same character, if they ever don't have the same character we then return false. If we loop through the entire thing and find they have the same characters throughtout, then it is a palindrome.

The following code solution doesn't follow that algorithm and instead checks to see if we reverse the string that we get the same result. This is still a valid solution however a bit more advanced and not does not test the appropriate concepts.

```python
class Solution:
    def isPalindrome(self, s: str) -> bool:
        new = ''
        for letter in s:
            if letter.isalpha() or letter.isdigit():
                new += letter.lower()
        return (new == new[::-1])
```
