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


