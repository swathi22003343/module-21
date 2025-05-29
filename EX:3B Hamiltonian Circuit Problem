# EX-3B Hamiltonian Circuit Problem

### DATE:

## AIM:
To write a python program to check whether Hamiltonian path exits in the given graph.

## ALGORITHM:

1. Initialize a 2D DP table dp[node][mask] to track if a path ending at node exists using vertices in mask.
2. For each node, set dp[node][1 << node] = True to represent paths starting from each node.
3. For all masks (subsets of nodes), check each node as a potential endpoint.
4. For each such node, loop through all other nodes to find a valid transition using the adjacency matrix.
5. If there is an edge and the previous state is valid, update the current dp value.
6. After filling the table, check if any dp[node][full_mask] is True, where full_mask = (1 << N) - 1.
7. If found, a Hamiltonian path exists.

## PROGRAM:

```
# Program to implement to check whether Hamiltonian path exits in the given graph.
# Developed by: SWATHI D
# Register Number: 212222230154
```
```

def Hamiltonian_path(adj, N):
    dp = [[False for _ in range(1 << N)] for _ in range(N)]

    for i in range(N):
        dp[i][1 << i] = True

    for i in range(1 << N):
        for j in range(N):
            if (i & (1 << j)) and any((i & (1 << k)) and adj[k][j] and j != k and dp[k][i ^ (1 << j)] for k in range(N)):
                dp[j][i] = True

    return any(dp[i][(1 << N) - 1] for i in range(N))
adj = [ [ 0, 1, 1, 1, 0 ] ,
        [ 1, 0, 1, 0, 1 ],
        [ 1, 1, 0, 1, 1 ],
        [ 1, 0, 1, 0, 0 ] ]
 
N = len(adj)
 
if (Hamiltonian_path(adj, N)):
    print("YES")
else:
    print("NO")
```

## OUTPUT:

![image](https://github.com/user-attachments/assets/cfbafcf2-9077-4323-a64c-d6141dc96abe)

## RESULT:
The Hamiltonian path program executed successfully, and it determined whether a Hamiltonian path exists in the given graph.
