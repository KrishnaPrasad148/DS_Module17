# Ex25 Adjacency List Representation
## DATE:
## AIM:
To write a C program to represent the given graph using the adjacency list.

## Algorithm
1. Read the number of vertices and number of edges.
2. Read all edge pairs (source and destination) and store them.
3. Create a graph using the input edge list.
4. Print the adjacency list representation of the graph.  

## Program:
```
/*
Program to find and display the priority of the operator in the given Postfix expression
Developed by: Krishna Prasad S
RegisterNumber:  212223230108
```
```c

int main(void)
{
    int n,i;
    scanf("%d",&N);
    scanf("%d",&n);
    struct Edge edges[n];
    for (i = 0; i < n; i++)
    {
        scanf("%d",&edges[i].src);
        scanf("%d",&edges[i].dest);
    }
   
    struct Graph *graph = createGraph(edges, n);
 
    printGraph(graph);
 
    return 0;
}

```

## Output:

![438606858-1cf60013-4b24-454e-a674-56704e72d3ac](https://github.com/user-attachments/assets/c6ea96b6-b3d1-4fd3-94cb-0bc15e350c23)


## Result:
Thus, the C program to represent the given graph using the adjacency list is implemented successfully
