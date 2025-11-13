- Variables arrays and assignments 
- 
# Branching 

## Conditional branching 
- Bool expressions are evaluated left t right 
- we use [[Glossary#Short Circuiting|Short Circuiting]] 
- we have two forms 
	- if ___ else 
	- if ___ then
## Goto  
- unconditional branching 


## Example
input a number n > 0 
output: true if n is even and false else 
currentVal ← n 
currentVal ← currentVal - 2 
if currentVal = 0 then 
	return true
if currentVal < 0 then 
	return false
else
	goto 2  
	