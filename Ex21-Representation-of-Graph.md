# Ex 21 Representation of Graph
## DATE: 21/04/2025
## AIM:
To write a C program to display the adjacency matrix of the given graph by supplying the edges and the number of vertices.

## Algorithm
1. Start the program.
2. Read the value of V (number of vertices).
3. Declare an adjacency matrix adjMatrix[V][V].
4. Initialize the matrix to 0 using the init function.
5. Calculate the maximum number of edges me as n * (n - 1) / 2.
6. For each edge, read e1 and e2, add the edge to the adjacency matrix, and stop if e1 == -1 && e2 == -1.
7. Print the adjacency matrix.
8. End the program.

## Program:
```
Program to display the adjacency matrix of the given graph
Developed by: Krishna Prasad S
RegisterNumber: 212223230108
```
```c

#include <stdio.h>

int V;

void init(int arr[][V]) {
    int i, j;
    for (i = 0; i < V; i++) {
        for (j = 0; j < V; j++) {
            arr[i][j] = 0;
        }
    }
}

void addEdge(int arr[][V], int e1, int e2) {
    arr[e1][e2] = 1;
    arr[e2][e1] = 1;
}

void printAdjMatrix(int arr[][V]) {
    int i, j;
    for (i = 0; i < V; i++) {
        for (j = 0; j < V; j++) {
            printf("%d ", arr[i][j]);
        }
        printf("\n");
    }
}

int main() {
    int e1, e2, me, n, i;
    scanf("%d", &V);

    int adjMatrix[V][V];
    init(adjMatrix);

    n = V;
    me = n * (n - 1) / 2;

    for (i = 0; i < me; i++) {
        scanf("%d%d", &e1, &e2);
        if (e1 == -1 && e2 == -1) {
            break;
        }
        addEdge(adjMatrix, e1, e2);
    }

    printAdjMatrix(adjMatrix);

    return 0;
}

```

## Output:
![438604009-0c816f26-fbf8-46a1-ad59-b0c0562c4e00](https://github.com/user-attachments/assets/a4f0a183-b76f-4094-9729-f4b807bcd908)


## Result:
Thus, the C program to print the adjacency matrix of the given graph is implemented successfully.
