2024-07-02 16:20

Status: 

Tags: #array #hashing 

# Valid Anagram

Given two strings `s` and `t`, return `true` *if* `t` *is an anagram of* `s`, and `false` otherwise

An Anagram is a word or phrase formed by rearranging the letters of a different word or phrase, typically using all the original letters exactly once. 

#### Example 1: 
	Input: s = "anagram", t = "nagaram"
	Output: true
#### Example 2: 
	Input: s = "rat", t = "car"
	Output: false

Constraints:
- $1 \leq$ `s.length`, `t.length` $\leq 5 * 10^4$
- `s` and `t` consist of lowercase English letters.

```python
class Solution(object):
	def is Anagram(self, s, t)
	"""
	:type s: str
	:type t: str
	:rtype: bool
	"""
	if len(s) != len(t):
		return False
	
	letter_count_s = {}
	letter_count_t = {}
	
	for letter in s:
		if letter not in letter_count_s:
			letter_count_s[letter] = 1
		else:
			letter_count_s[letter] += 1
	
	for letter in t: 
		if letter not in letter_count_t:
			letter_count_t[letter] = 1
		else:
			letter_count_t[letter] += 1
	
	return letter_count_s == letter_count_t
```

We can use the data structure a [[HashMap]] where each value in the set contains a hash value which ensures that only unique values are in the set. 

To check if the two strings are anagrams of each other we first need to check if they are the same length, if they aren't its then impossible for them to be a solution of each other. After this we create 2 different [[HashMap]]s and add all the count of letters of each word. After this we can check if the letter counts of both words are equivaliant, if they are we return true that this is a anagram, if not we return false that this is not a anagram. 