---
id: Valid Sudoku
aliases:
  - Valid Sudoku
tags: []
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

This should need only diagonal check, horizontal check and vertical check to see if all the correct amount of numbers are in the grid and then to reference the entire row/col to see if the board is valid or not. 

