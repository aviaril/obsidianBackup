- [ ] 
# Static data Structures 
- You cannot change the size of static data structures while the program is running.
## Arrays
Arrays are static (not always implemented that way)
Size of arrays is fixed so we need to know the upper limit of the number of elements
inserting a new element is expensive 
- Easy to store in cache 


# Dynamic data structures
- allow us to increase the size of the structure while the program is running 

## Linked list 
Each element is a data item and a pointer to the next element
Allows you the list to grow as needed 
- Elements are not stored in contiguous memory 
- To search a linked list the you need to start from the first node and follow pointers so you cannot directly access and element 
- New nodes can be added anywhere in memory 
- The bigger it grows the longer it takes to search (It is O(n))

- Need extra memory space for the pointer 
- When you change the position of a list element you do not change the location of the data you just change the pointer, This also goes for deleting data from the list, 

## Hash Tables
- A hashing algorithm is used on a field to generate an address where the data will be stored
- This can result in a collision where more than on item has the same address, to overcome this linear probing or chaining can be used
- O1
#### Linear Probing
- if the address already has data in it you move thought the structure until a free space is found 
- When you search you start at the location the equation gives you and then continue to search sequentially  form that point 
#### Chaining 
- Each location on the hash table points to a liked list 
- New item is stored in the next location of the linked list, when searching you go to the liked list at the location and then search though the list 
- This also means that there is no upper limit on the size of the table 
#### Overflow 
- You can also just put all of the collided data into an overflow area that you search though, however this is extremely inefficient.  
# Trees
Queues, stacks, arrays and linked lists are linear lists meaning the data items point to the next item. Different to all of this the tree is designed to represent the relationship between data items. 
- The tree is a collection of nodes connected by directed edges.
- It is a non-linear data structure
- Can be empty or can be structures with a root node and zero or more subtrees 
- Each node can have a number of children, nodes with no children are called leaves or external nodes, if a node has at least one child it is called an internal node. 
- The depth of a nod is the number of edges from the root to the node 
- the hight of the node is the number of edges between the deepest leaf connected to it. 
- Often used to model file systems 
- pointers are used to allow transversal 
### Traversing a tree
#### Depth first search
-Follow the pointers down as far as possible then backtrack and take the next route 
#### Breadth first search
go down one edge on every branch coming from the node and then repeat for every layer of the tree
## Binary Trees
- Binary trees are constructed to be easily searched, this is done by arranging the data in the nodes so that the parent is greater than or equal to the left descendant and less than the right descendant
- When filling a binary tree you take the piece of information and compare the value of the added information to the data in that node, if it is greater move to the right, if it is less move to the left and repeat until an empty spot is found, then add the data there.
### Traversing a binary tree
There are three methods, post order, pre order, in order
#### In order traversal 
- Traverse the left sub-tree 
- Visit the root
- Traverse the right sub-tree
- give results in order
#### Pre-order traversal
- start at root
- traverse left sub-tree
- Traverse right sub-tree
#### Post-Order traversal
- Traverse the left sub-tree
- Traverse the right sub-tree
- End at the root
- often used to delete the tree
### Usage
- storing sorted and related data items
- representing the order mathematical equations are evaluated in 

### Implementation
- can be implemented using arrays, classes, tuples, records
- to implement you need a left pointer, right pointer and a data item
#### Implementing with arrays

| array    | left | data | right |
| -------- | ---- | ---- | ----- |
| Tree[0]  | 1    | 17   | 4     |
| Tree[1]  | 2    | 8    | 3     |
| Tree[2]  | NULL | 4    | 7     |
| Tree[3]  | NULL | 12   | 6     |
| Tree[4]  | 5    | 22   | 8     |
| Tree[5]  | NULL | 19   | NULL  |
| Tree[6]  | NULL | 14   | NULL  |
| Tree[7]  | NULL | 5    | NULL  |
| Tree[8]  | 9    | 30   | NULL  |
| Tree[9]  | NULL | 25   | NULL  |
| Tree[10] | NULL | NULL | NULL  |
| Tree[11] | NULL | NULL | NULL  |

| array    | left | data    | right |
| -------- | ---- | ------- | ----- |
| Tree[0]  | 3    | Monkey  | 1     |
| Tree[1]  | 2    | Topi    | 5     |
| Tree[2]  |      | Ostrich | 8     |
| Tree[3]  |      | Giraffe | 4     |
| Tree[4]  |      | Hippo   | 10    |
| Tree[5]  |      | Zebra   | NULL  |
| Tree[6]  |      | Buffalo | 7     |
| Tree[7]  |      | Cheetah | NULL  |
| Tree[8]  |      | Rhino   | NULL  |
| Tree[9]  |      | Baboon  | NULL  |
| Tree[10] |      | Jackal  | NULL  |
| Tree[11] | NULL | NULL    | NULL  |
|          | NULL | NULL    | NULL  |
|          | NULL | NULL    | NULL  |
|          | NULL | NULL    | NULL  |
# Graphs
- used to represent complex structures such as Networks and bandwidth, Maps, Webpages and links
- Set of nodes (vertices) connected by edges (arcs)
- can be directed meaning the flow/travel can only go in one direction 
- Edges can be weighted to show that there is a cost to go from one node to another

##### adjacency matrix 
- undirected graphs can be shown in an adjacency matrix where there is a 1 if there is a link and a 0 if there is not
- undirected graphs show the weight of the edge instead of a binary 1 or 0

task show a directed graph as an adjacency matrix


|     | A   | B   | C   | D   | E   | F   |
| --- | --- | --- | --- | --- | --- | --- |
| A   |     | 5   | 4   |     |     |     |
| B   |     |     | 6   | 3   |     |     |
| C   |     |     |     |     |     | 8   |
| D   |     |     |     |     | 2   |     |
| E   |     |     |     |     |     |     |
| F   |     |     |     |     |     |     |
### Traversing a graph
#### Depth first
Go as far down one route as possible before backtracking and taking the next route. 
We move down the route and add the visited nodes to a stack in the order that we visit the nodes, once we get to the end of the route we mark the last node in the route as searched and add that to the searched nodes stack. After this we start to backtrack to the last node with a new branch, and go down this secondary route, we then repeat the above method 
1. put any node on the top of a stack 
2. Take the top item of the stack and add it to the visited list 
3. Create a list of that vertex's adjacent nodes. Add the ones which aren't in the visited list to the top of the stack
4. Repat steps two and three until the stack is empty 
Useful for mazes and scheduling jobs

#### Breadth first 
start at A and visit all adjacent nodes before visiting B and repeating the process for each level.  
1. Visit the adjacent unvisited vertex mark it as visited and add it to the queue 
2. if no adjacent vertex is found remove the first vertex from the queue
3. Repeat 1 and 2 until the queue is empty 
good for finding the shortest path in things like GPS systems