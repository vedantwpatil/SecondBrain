---
id: Valid Sudoku
aliases:
  - Valid Sudoku
tags:
  - array
  - hashing
  - medium
---

2024-07-02 16:19

Status: 

Tags: #array #hashing 

# Valid Sudoku

You are given a 9x9 Sudoku board, `board`. A sudoku board is valid if the following rules are followed: 
1. Each row must contain the digits `1-9` without duplicates 
2. Each column must contain the digits `1-9`without duplicates
3. Each of the nine `3x3` sub-boxes of the grid must contain the digits `1-9` without duplicates. 

Return `true` if the sudoku board is valid, otherwise return `false`

Notes: A board does not need to be full or solvable to be valid. 

### Example 1: 
```python

Input: board = 
[["1","2",".",".","3",".",".",".","."],
 ["4",".",".","5",".",".",".",".","."],
 [".","9","8",".",".",".",".",".","3"],
 ["5",".",".",".","6",".",".",".","4"],
 [".",".",".","8",".","3",".",".","5"],
 ["7",".",".",".","2",".",".",".","6"],
 [".",".",".",".",".",".","2",".","."],
 [".",".",".","4","1","9",".",".","8"],
 [".",".",".",".","8",".",".","7","9"]]

Output: true
```
### Example 2: 
```python

Input: board = 
[["1","2",".",".","3",".",".",".","."],
 ["4",".",".","5",".",".",".",".","."],
 [".","9","1",".",".",".",".",".","3"],
 ["5",".",".",".","6",".",".",".","4"],
 [".",".",".","8",".","3",".",".","5"],
 ["7",".",".",".","2",".",".",".","6"],
 [".",".",".",".",".",".","2",".","."],
 [".",".",".","4","1","9",".",".","8"],
 [".",".",".",".","8",".",".","7","9"]]

Output: false
```
Explanation: There are two 1's in the top-left 3x3 sub-box 

### Constraints: 
- `board.length == 9`
- `board[i].length == 9`
- `board[i][j] is a digit 1-9 or '.'`

### Thought Process/Rough Work:

This should need only horizontal check and vertical check to see if all the correct amount of numbers are in the grid and then to reference the entire row/col to see if the board is valid or not. 

The way we would check this is loop through the entire entry and add all the values to a hashset, if we add something and it returns false then we return false for the entire thing. Otherwise if we go through all our checks and there are no issues, we then return true. 

Alternativly we could also add everything to the hashset and compare with the length of the hashset and the length of entrys but that would be unecessary and there is a more efficent way of doing it.

### Solution: 
Time Complexity: O(9^2)
Space Complexity: O(9^2) 

```python
class Solution: 
    def isValidSodoku(self, board: List[List[str]]) -> bool:
        cols = collections.defaultdict(set)
        rows = collections.defaultdict(set)
        squares = collections.defaultdict(set) 

        for r in range(9):
            for c in range(9):
                if board[r][c] == ".":
                    continue
                elif (board[r][c] in rows[r] or board[r][c] in cols[c] or board[r][c] in squares[(r//3, c//3)]):
                    return False
                cols[c].add(board[r][c])
                rows[r].add(board[r][c])
                squares[(r // 3, c //3)] .add(board[r][c])

        return True
```

### Explaination:
We create several hashsets because they are the most convenient data structure for this question. We go and loop through the entire board and check to see if the spot is empty or not, if it is empty then we can ignore it. If the spot is not empty we then check to see if it already exists in one of our hashsets, if it does we return false saying that this is not a valid soduku board and if it is true then we continue updating our hashset. Finally if we go through the entire board without finding any issue we then return true. 

**Note:** We use r//3 and c//3 to be able to locate the different squares which are present in the grid. This way we are able to access each square and check if they contain duplicate elements in the same square. 
