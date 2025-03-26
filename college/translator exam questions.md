1. Assembler 
2. Assembler 
3. Assembler
4. ⠀
	1. To convert human readable code to machine code so that it can be run 
	2. ⠀
		1. A compiler outputs an executable while an interpreter just runs a source code file 
		2. An interpreter will run a program line by line and stop when it finds an error while a compiler will attempt to compile the entire program and then output all errors at the end of compilation 
5. ⠀
	1. Compiler, interpreter, compiler, interpreter
	2. ⠀
		1. Compiler 
		2. The code will need to be executed quickly 
	3. 
		```
		01 inp 
		02 sta NumA
		03 inp 
		04 sta NumB
		05 lda zero
		06 sta answer
		07 lda answer
		08 ADD NumA
		09 sta answer 
		10 lda numB
		11 SUB one
		12 sta numB
		13 brz 15
		14 bra 07
		15 zero DAT 0
		16 one DAT 1
		17 NumA DAT
		18 NumB DAT
		```
6. Compiled programs are executables, this means that the source code is not given to the end user so that they can not access it. 
7. C++ is compiled to machine code, 