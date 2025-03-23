1. consider first element to be sorted 
2. compare next element to the sorted element 
3. If the next element is smaller compare it to the next element and continue until you find the correct space 
4. if it is larger consider it sorted and move to the next 

## Example 
| denotes where the sorted numbers end 
smallest to largest

| 5\| | 2   | 7   | 3   | 9   | 6   |
| --- | --- | --- | --- | --- | --- |
| 2   | 5\| | 7   | 3   | 9   | 6   |
| 2   | 5   | 7\| | 3   | 9   | 6   |
| 2   | 3   | 5   | 7\| | 9   | 6   |
| 2   | 3   | 5   | 7   | 9\| | 6   |
| 2   | 3   | 5   | 6   | 7   | 9\| |

