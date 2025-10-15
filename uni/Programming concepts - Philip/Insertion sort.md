[[Algorithms]]
# Algorithm 
input: a list *l* of numbers (n ≥ 0)
output: a list of the same numbers sorted into ascending order 
- look at each value in turn 
- after moving everything to the left is sorted 
##### Needs checking
1. consider first element to be sorted 
2. compare next unsorted element to the previous element 
	1. If the unsorted element is smaller compare it to the next sorted element and continue until you find the correct space 
3. if it is larger consider it sorted and move to the next 

### Example 
| denotes where the sorted numbers end 
smallest to largest

| 5\| | 2   | 7   | 3   | 9   | 6   |
| --- | --- | --- | --- | --- | --- |
| 2   | 5\| | 7   | 3   | 9   | 6   |
| 2   | 5   | 7\| | 3   | 9   | 6   |
| 2   | 3   | 5   | 7\| | 9   | 6   |
| 2   | 3   | 5   | 7   | 9\| | 6   |
| 2   | 3   | 5   | 6   | 7   | 9\| |

--- 
 