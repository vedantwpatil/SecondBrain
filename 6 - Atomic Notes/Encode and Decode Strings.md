---
id: String Encode and Decode
aliases:
  - String Encode and Decode
tags: []
---

# String Encode and Decode

Design an algorithm to encode a list of strings to a single string. The encoded string is then decoded back to the original list of strings.

Please implement encode and decode. 

### Example 1: 
```python
Input: ["neet","code","love","you"]
Output:["neet","code","love","you"]
```
### Example 2: 
```python
Input: ["we","say",":","yes"]
Output: ["we","say",":","yes"]
```
### Constrains: 
- 0 <= `strs.length` < 100
- 0 <= `strs[i].length` < 200
- `strs[i]` contains only UTF-8 characters.

### Rough Work/Thought Process: 
We can be given any kind of character in our strings which makes things difficult as we originally would consider joining the words together with a symbol in between that we would then check for in the next algorithm, however we would be unable to differentiate between the symbol and the rest of the characters in the rest of the cases. 

We could go about this by storing the amount of letters in a array however that is not something the solution wants so we have to go about it in a different way.  

Something we can do is insert information at the beginning of our string about the string with a special character in between to know when the information starts and when the actual word starts.  

### Solution: 
Time Complexity: O(n)
```python 

class Solution:

    def encode(self, strs: List[str]) -> str:
        res = ""
        for s in strs: 
            res += str(len(s)) + "$" + s
        return res 

    def decode(self, s: str) -> List[str]:
        res, i = [], 0

        while i < len(str): 
            j = i 
            while str[j] != "$":
                j+= 1
            length = int(str[i:j])
            res.append(str[j+1 : j+1+length])
            i = j + 1 + length 
        return res

```
### Explanation: 
To solve this we are inputting information at the beginning of each of the string in our encode method to know how long the string is and how many characters we need for our string. We put a special character in between the number of information and the rest of the string to know if that the number is not apart of the string and will instead tell us the information about the word. This works because by inputting at the start of the string there aren't any other characters which could confuse us and even if the special character we choose is in the string, we only need to check for the first instance of it for us to know the information about the string. 

Decode is more complicated with us creating 2 pointers, one starts at the beginning of the string and we are checking for the special character we choose in our encode method. Once we find that character, we know that the length of that string is the number between our first pointer and the second pointer and now we can append those characters in this length as their own string and continue on to the next. 

