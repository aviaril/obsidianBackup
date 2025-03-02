A+ = A* , cant have asterisk 

# Dijkstra's

#### 1.

| Node | distance | prev |
| ---- | -------- | ---- |
| A    | 0        | N/A  |
| B    | 2        | A    |
| C    | 3        | B    |
| D    | 6        | A    |
| E    | 10       | D    |
#### 2. 
| Node | distance | prev |
| ---- | -------- | ---- |
| A    | 0        | N/A  |
| B    | 2        | A    |
| C    | 3        | A    |
| D    | 4        | C    |
| E    | 5        | C    |
| F    | 7        | E    |
| G    | 11       | F    |
# A*
| Node | distance (G) | heuristic (H) | F = G + H | prev |
| ---- | ------------ | ------------- | --------- | ---- |
| A    | 0            | 30            | 30        | N/A  |
| B    | 12           | 18            | 30        | A    |
| C    | 7            | 12            | 19        | A    |
| D    | 4            | 20            | 24        | A    |
| E    | 6            | 8             | 14        | C    |
| F    | 11           | 0             | 11        | B    |