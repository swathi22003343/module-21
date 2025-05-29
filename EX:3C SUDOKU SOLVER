# EX:3C SUDOKU SOLVER

### DATE:

## AIM:
To write a python program to find the solution of sudoku puzzle using Backtracking.

## ALGORITHM:

1. Traverse each cell of the Sudoku board.
2. When an empty cell (0) is found, try all digits from 1 to 9.
3. For each digit, check if it is safe to place (not in same row, column, or 3×3 subgrid).
4. If safe, place the digit and recursively solve the rest of the board.
5. If placing the digit leads to no solution, reset the cell and backtrack.
6. If all cells are filled without conflict, print the solved board.

## PROGRAM:

```
# Program to implement to to find the solution of sudoku puzzle using Backtracking.
# Developed by: SWATHI D
# Register Number: 212222230154

board = [
    [0, 0, 0, 8, 0, 0, 4, 0, 3],
    [2, 0, 0, 0, 0, 4, 8, 9, 0],
    [0, 9, 0, 0, 0, 0, 0, 0, 2],
    [0, 0, 0, 0, 2, 9, 0, 1, 0],
    [0, 0, 0, 0, 0, 0, 0, 0, 0],
    [0, 7, 0, 6, 5, 0, 0, 0, 0],
    [9, 0, 0, 0, 0, 0, 0, 8, 0],
    [0, 6, 2, 7, 0, 0, 0, 0, 1],
    [4, 0, 3, 0, 0, 6, 0, 0, 0]
]
def printBoard(board):
    for i in range(0, 9):
        for j in range(0, 9):
            print(board[i][j], end=" ")
        print()
def isPossible(board, row, col, val):
    for j in range(0, 9):
        if board[row][j] == val:
            return False
    for i in range(0, 9):
        if board[i][col] == val:
            return False
    startRow = (row // 3) * 3
    startCol = (col // 3) * 3
    for i in range(0, 3):
        for j in range(0, 3):
            if board[startRow+i][startCol+j] == val:
                return False
    return True
def solve():
    for row in range(9):
        for col in range(9):
            if board[row][col] == 0:
                for val in range(1, 10):
                    if isPossible(board, row, col, val):
                        board[row][col] = val
                        solve()
                        board[row][col] = 0
                return
    printBoard(board)
solve()
```

## OUTPUT:

![image](https://github.com/user-attachments/assets/e5783380-31b4-4230-bce0-183a6b13d93a)

## RESULT:
The Sudoku solver program executed successfully and found the solution for the given puzzle.
