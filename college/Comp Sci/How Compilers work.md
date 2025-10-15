
### Types of Error
#### Logical error 
Code is Syntactically correct but there is an error in the method / typo e.g. used < instead of > or / instead of %
#### Syntax error 
A section of the code does not confirm with the rules of the language e.g. opening bracket but no closing bracket or no semi colon. also includes typos in method names e.g. prentf instead of printf 
#### RunTime Error 
The code is syntactically correct but creates an error when run e.g. divide by zero or a stack overflow. 

Only syntax errors will be picked up by the compiler. 

# Lexical analysis 
- Identifying each atomic item (Lexeme) 
- Creating a symbol table
	- Used for keywords 
	- Each symbol is a sting of binary digits of fixed length 
- The table list each available token and what type of symbol it is 

Types of token can be divided into 
1. Language defined tokens 
	- Reserved words,
	- operators,
	- keywords 
2. User defined tokens 
	- Identifiers - names of variables, procedures
	- Literals - numbers strings, etc 
Lexical analysis removes comments and whitespace 
##### Example 
sum = 3 + 2; 

| lexeme | token type          |
| ------ | ------------------- |
| sum    | identifier          |
| =      | Assignment operator |
| 3      | Integer literal     |
| +      | Addition Operator   |
| 2      | Integer literal     |
| ;      | End of statement    |

# Syntactic and semantic analysis
- Accepts output from lexical analysis 
- this is checked against the rules of the language 
- errors are reported as a list and outputted at the end of compilation 
- diagnostics may be given but not necessarily 
- if no errors code is passed to the code generation stage

- includes semantic analysis which covers thing such as;
	- x being declared multiple times 
produces an abstract syntax tree to pass to the code generation stage 
# Code generation 
- Produces machine code/executable equivalent to the source code 
- Variables/constants are given addresses 
- Relative addresses are calculated 
### Optimisation 
- Makes code more efficient 
- increases execution speed or reduces space 
- number of instructions are reduced 
- can choose to optimise for speed or size
- includes 
	- loop optimisation 
	- Makes calculations more efficient 
	- Change relative addresses to absolute

### Linkers 
- Program that takes one or more object files and combines them into a single executable, lib or object file. This is called static linking 
	- may require more disk space and memory than dynamic but is faster and more portable 
	- does not require presence of a library of the system running the program 
- Dynamic linker - part of OS that loads and link shared libraries (DLLs) for an executable 
	- Linking does not happen until image is run 
	- multiple programs can share the same copy of a library 

### Loaders 
- Part of OS that loads programs and libraries 
- places programs into memory and preps them for execution 
- Once a program is loaded into memory and prepped control is passed to it 