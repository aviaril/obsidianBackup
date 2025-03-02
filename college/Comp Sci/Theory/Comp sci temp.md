To find if pug is in the binary search tree you will start at the root 'Harrier' and compare the first letters, because 'p' comes after 'h' you will the follow the pointer to the right and repeat this. The next node contains 'Rottweiler' because 'p' comes before 'r' you will follow the pointer left where you will find 'Pug'.

To determine if 'Spaniel' is in the tree you would repeat the same steps as searching for 'Pug', compare to the root and move to the right, then compare to rottweiler and 



To add a new item of data to a binary tree you will start by finding where in the tree it needs to go. This is done by comparing the new item to the root node, if the new item is larger than the data in the root follow the pointer to the right child node, if it is less than or equal to the data in the root follow the pointer to the left child node; From here repat the comparisons to the data in the nodes until there is no child node to move to, when there is no child node to move to change the pointer of the current node from the termination point to a pointer to a new node and place the new data in this new node. 
# Graphs and trees
1. Similarity 1: Both trees and graphs are based on the concept of nodes (or vertices) connected by edges. 
	Similarity 2: 
	Difference 1: Trees must start from a root node while graphs do not have to 
	Difference 2: Graphs can be directional and have weights assigned to their edges while trees cannot 
2. On this binary tree a breadth first traversal would start by visiting the M node and adding it to a queue, after this you would visit every node adjacent to the M nodes, in this case E then S 
3. 
	a. 
		1. A directed graph has directions on the edges meaning the edge can only be traversed in one direction e.g. if there was a directional edge between A and B you could traverse form A to B but not B to A.
		2. Graphs can have weights added to there edges while trees cannot. 
	b. The graph is a visualisation of the problem because the nodes do not simulate a shape they are just a system of pointers 
4. In order the DE-Duplicator will visit 'accounts.doc', 'budget.xls', 'beach.jpg', 'hotel.jpg' , 'sunset.jpg' and finally 'tournament.jpg' 
5. 5.
	a. 
		1. A depth first traversal is performed by starting at the deepest leaf of the graph, if there are multiple leaves on the same level use the leftmost leaf. From the deepest leaf move up to its parent and check of there are any children other than the one we came from, if there are they will come after the parent of the original 