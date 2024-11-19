## Introduction - needs re-written
Combination locks are incredibly useful devices that allow the user to secure containers, doors, bikes etc against theft or damage. Adding to their utility they do not even need a key meaning individuals do not need to worry about carrying or losing one and companies to not need to pay to issue every employee  or However many of them are critically flawed, able to be bypassed in seconds with the right tools, another issue is that given enough time an attacker may have time to simply guess the code. 
## Concept
If my lock were to be mounted on a wall the user would see 
## Subsystem 1 - Dials 
### Design
A single dial has to output a logic high signal when the resistance of a potentiometer($R_i$) is between two values and output low when the resistance is not between these two values. The values needed to output high are controlled by a separate potentiometer I am calling the setting potentiometer ($R_{vs}$ Symbol may need changing), the setting potentiometer will have the same maximum resistance as the input potentiometer making the desired value easier to set. To compare the values of the potentiometers I use two comparators, comparator 1 has $R_{vs}$ connected to the 
 
#### Parts List (Per Dial)
- 1KΩ resistor x3
- Lm311 Comparator x2 
- 10KΩ potentiometer x2
- Diode x1 
- Quad Nand gate (1 per four dials)

# Building Errors 
### Dials
While building the first dial subsystem I placed the collector resistor of the second comparator in the wrong place, instead of placing it between the collector and the +5V rail I placed it between the Vcc of the LM311 chip and the +5V rail. This resulted in the comparator outputting +1.5V when high instead of +5V, this was not enough to trigger the AND gate so the subsystem never had a final output of Logic High as it should when the potentiometer is in the correct position. 
(The Collector resistor in the incorrect place, it should have been in row 24 next to the red wire)
![[Resistor error.png]]
## Subsystem ??? - Solenoid 
The basic idea behind the subsystem is that the solenoid will 