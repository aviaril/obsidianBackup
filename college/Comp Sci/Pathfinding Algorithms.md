# Shortest route 
Abstract map to group of nodes representing locations connected to each other. 
Weight the links between nodes based no the distance in real life. 

# Dijkstra's algorithm 
- mark the start node as 0 distance from itself and all others as an infinite distance from teh start node 
- While destination node is unvisited:
	- go to closest node to the start node and call this the current node 
	- for every unvisited node connected to current:
		- calculate distance 

###### <span style="color:rgb(255, 92, 0)">Practice 1</span>

| Node | Distance | Prev |
| ---- | -------- | ---- |
| A    | 0        | N/A  |
| B    | 75       | A    |
| C    | 10       | A    |
| D    | 80       | B    |
| E    | 65       | C    |
| F    | 40       | C    |
| G    | 50       | F    |
| H    | 90       | G    |
| I    | 90       | D    |
| J    | 105      | H    |

A-C-F-G-H-J 
## A* algorithm 
- based on Dijkstra's, in some cases the same
- can give some false results if there are a large amount of intermediate nodes 

### Heuristics 
- UPS route planner adds time to unload the package and the time to get to the door, the day of the week, and maximises right turns (American)
- A* uses heuristics (uses existing experience to form a solution)

#### Algorithm 
- begin at start and make it current
- while destination is unvisited:
	- For each node connected to current 
		- Add to list of open nodes 
		- add distance from start (g) to heuristic estimate of distance left (h)
		- assign this value (f) to the node 
	- make unvisited node with the lowest value the current node 