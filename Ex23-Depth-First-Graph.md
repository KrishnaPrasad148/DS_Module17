# Ex23 Depth First Graph
## DATE: 
## AIM:
To compose the code for the function createNode to traverse the graph below in the depth first fashion.

![image](https://github.com/user-attachments/assets/63552824-d0a3-49c6-a473-6db27d1f03e4)

## Algorithm
1. 1. Start
2. Allocate memory for a new node.
3. Set the vertex field of the new node to the given value v.
4. Set the next pointer of the new node to NULL.
5. Return the newly created node, and end it.
## Program:
```
Program to traverse the graph below in the depth first fashion
Developed by: Krishna Prasad S
RegisterNumber: 212223230108
```
```c

/*#include<stdio.h>
#include<stdlib.h>
struct node{
int vertex;
struct node* next;
};
struct node*createNode(int v);

struct Graph {
int numVertices;
int* visited;
struct node** adjLists;
};*/

struct node*createNode(int v)
{
  struct node* newNode=malloc(sizeof(struct node));
  newNode->vertex=v;
  newNode->next=NULL;
  return newNode;
}

```

## Output:

![438606086-5896c580-b2c3-4aeb-8a4c-57be4a0d2c8b](https://github.com/user-attachments/assets/762f967b-cfb1-4bdb-8d04-b28212e7a188)


## Result:
Thus, the C code for the function createNode to traverse the graph below in the depth first fashion is implemented successfully
