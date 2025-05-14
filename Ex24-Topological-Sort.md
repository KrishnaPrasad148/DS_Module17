# Ex24 Topological Sort
## DATE:  24/04/2025
## AIM:
To compose the code to determine whether the topological ordering for the following graph is possible or not.

![image](https://github.com/user-attachments/assets/c74a7111-9b59-475c-aad4-9baf23d50ec0)


## Algorithm
1. Start and create the graph using create_graph().
2. Calculate indegrees; enqueue vertices with indegree 0.
3. Initialize count and process vertices from the queue.
4. For each vertex, dequeue, add to topo_order, update adjacent vertices' indegrees, and enqueue if indegree becomes 0.
5 .If a cycle exists, print error; else, print topological order and end.  

## Program:
```
Program to determine whether the topological ordering for the following graph is possible or not
Developed by: Krishna Prasad S
RegisterNumber:  212223230108
```
```c

//#include<stdio.h>
//#include<stdlib.h>
//#define MAX5
//int n; /*Number ofverticesinthegraph*/
//int adj[MAX][MAX];/*AdjacencyMatrix*/
//void create_graph();
//int queue[MAX], front =-1,rear =-1;
//void insert_queue(int v);
//int delete_queue();
//int isEmpty_queue();
//int indegree(int v);

int main()
{
        int i,v,count,topo_order[MAX],indeg[MAX];

        create_graph();

        /*Find the indegree of each vertex*/
        for(i=0;i<n;i++)
        {
                indeg[i] = indegree(i);
                if( indeg[i] == 0 )
                        insert_queue(i);
        }

        count = 0;

        while(  !isEmpty_queue( ) && count < n )
        {
                v = delete_queue();
        topo_order[++count] = v; /*Add vertex v to topo_order array*/
                /*Delete all edges going from vertex v */
                for(i=0; i<n; i++)
                {
                        if(adj[v][i] == 1)
                        {
                                adj[v][i] = 0;
                                indeg[i] = indeg[i]-1;
                                if(indeg[i] == 0)
                                        insert_queue(i);
                        }
                }
        }

        if( count < n )
        {
                printf("No topological ordering possible, graph contains cycle\n");
                exit(1);
        }
        printf("Vertices in topological order are :\n");
        for(i=1; i<=count; i++)
                printf( "%d ",topo_order[i] );
        printf("\n");

        return 0;
}

```

## Output:

![438606442-087b9072-74cc-44ad-95a0-4de7a19fada5](https://github.com/user-attachments/assets/8a886084-6c29-4fa0-bdb2-7cbe8c4a4c24)


## Result:
Thus, the C program for determining whether the topological ordering for the following graph is possible or not, is implemented successfully.
