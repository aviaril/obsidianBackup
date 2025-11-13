[[Conditionals]]
### For-each loop
#### structure
for( ElementType element : collection){
	loop body statements 
} 
#### example
public void listNotes(){
	for(String note : notes){
		System.out.println(note);
	}
}
- for each note in notes print the value of the note 
- different from a for each loop 
### For loop
#### structure  
for(initialization; condition; post-body action){
	body 
}
#### example 
for(i=0;i<10;i++){
	System.out.println("Hello World");
}
- its a for loop
### while 
#### structure 
while (condition){
	statement;
}
#### example 
while (i < 5){
	System.out.println(i);
	i++;
}
- You know what a while loop is 
## iterator objects
#### example
public void listNotes()  
{  
	Iterator\<String> it = notes.iterator();  
	while(it.hasNext()) {  
		System.out.println(it.next());  
	}  
}
- while the collection has a next element print the next element
