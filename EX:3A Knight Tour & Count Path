# EX:3A Knight Tour & Count Path

### DATE:

## AIM:
To write a python program to find minimum steps to reach to specific cell in minimum moves by knight

## ALGORITHM:

1. Define all 8 possible moves of a knight using dx and dy arrays.
2. Create a queue and enqueue the knight's initial position with distance 0.
3. Mark the initial position as visited.
4. While the queue is not empty, dequeue the front cell.
5. If the current cell is the target position, return its distance.
6. For each of the 8 possible knight moves, check if the new position is within bounds and not visited.
7. If valid, mark it as visited and enqueue it with distance incremented by 1.
8. Repeat the process until the target is found or the queue becomes empty.
9. If the target is unreachable, return infinity (inf).
    
## PROGRAM:

```
# Program to implement to find minimum steps to reach to specific cell in minimum moves by knight.
# Developed by: SWATHI D
# Register Number: 212222230154
```
```

class cell:
    def __init__(self, x = 0, y = 0, dist = 0):
        self.x = x
        self.y = y
        self.dist = dist
def isInside(x, y, N):
    if (x >= 1 and x <= N and
        y >= 1 and y <= N):
        return True
    return False
def minStepToReachTarget(knightpos,targetpos, N):
    dx = [-2, -1, 1, 2, -2, -1, 1, 2]
    dy = [-1, -2, -2, -1, 1, 2, 2, 1]
    queue = []
    queue.append(cell(knightpos[0], knightpos[1], 0))
    visited = [[False for _ in range(N + 1)] for _ in range(N + 1)]
    visited[knightpos[0]][knightpos[1]] = True
    while len(queue) > 0:
        curr = queue.pop(0)
        if curr.x == targetpos[0] and curr.y == targetpos[1]:
            return curr.dist
        for i in range(8):
            x = curr.x + dx[i]
            y = curr.y + dy[i]
            if isInside(x, y, N) and not visited[x][y]:
                visited[x][y] = True
                queue.append(cell(x, y, curr.dist + 1))
    return float('inf')
if __name__=='__main__':
    N = 30
    knightpos = [1, 1]
    targetpos = [30, 30]
    print(minStepToReachTarget(knightpos,targetpos,N))
```

## OUTPUT:

![image](https://github.com/user-attachments/assets/fad57299-a769-4b1c-9fb8-8b6e00425f13)

## RESULT:
The program executed successfully, and the minimum number of steps for the knight to reach the target was calculated.
