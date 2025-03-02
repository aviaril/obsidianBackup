combines instructions and data into a self sufficient object that can be used within a program 

##### classes and objects 
- the class contains the template for an object and information about what defines an object
- the object is a runtime representation of the class, an instance 
- creating an object is called instantiating
#### Inheriance 
- a sub class will inherit 


### Pseudocode task 
Class GeometricObject 
	private string Colour
	private bool Filled
	private dateCreated 
	public procedure new(colour, filled, dateCreated)
	public method getColour()
	return colour
	public function isFilled()
	return filled
	public procedure setColour(newCcolour)
	colour = newColour
	end procedure
	filled = isfilled()
	
	
end procedure 

Class Circle inherits GeometricObject 
	private double radius
public Circle new(circle)

Class Rectangle inherits GeometricObject 
	private double width 
	private double height 
### Encapsulation
- The inclusion of all of the resources (methods and data) needed by an object within that object. 
- getters are functions setters are procedures 
- Makes sure that other classes can only alter an attribute in the intended way 
- Stops attributes from being accidentally changed on other class's methods. 
### instantiation 
- 