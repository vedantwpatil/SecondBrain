---
id: Group Anagrams
aliases: []
tags: []
---

2024-07-02 16:20

Status: 

Tags: #hashing #array 

# Group Anagrams

Given an array of strings `strs`, group the anagrams together. You can return the answer in any order. 

An Anagram is a word or phrase formed by rearranging the letters of a different word or phrase, typically using all the original letters exactly once.

### Example 1:
```python

Input: strs = ["eat","tea","tan","ate","nat","bat"]
Output: [["bat"],["nat","tan"],["ate","eat","tea"]]
```
### Example 2:
```python

Input: strs = [""]
Output: [[""]]
```
### Example 3: 
```python

Input: strs = ["a"]
Output: [["a"]]
```
### Constraints:

1 <= `strs.length` <= 10^4
0 <= `strs[i].length`` <= 100
`strs[i]` consists of lowercase English letters.

### Rough Work/Thought Process: 

Since we are trying to make anagrams, we need to count how many letters are in each word and group those words together. We should go through the list, count the letters in a hashmap and then group all the words with the same amount of letters together. 

Not really sure on how to return the strings together 
### Solution:
Time Complexity: O(m*n)
```python

class Solution(object):
    def groupAnagrams(self, strs):
        """
        :type strs: List[str]
        :rtype: List[List[str]]
        """
        returnHash = collections.defaultdict(list)

        for word in strs:
            count = [0] * 26
            
            for letter in word:
                count[ord(letter) - ord("a")] += 1
            returnHash[tuple(count)].append(word)
        return returnHash.values()
```
### Explanation: 

In our code we create out hasmap and we count how many character in each word by using an array, we only need to worry about lowercase letters so we only need 26 characters. We use `ord()` to find the ascii value of both of the characters to map it to the correct index. With this we then increament our count with the index being the ascii value of each letter. We then group all strings together which have the same amount of letters and append them to a hashMap. After this we then return those groups as our final string 
