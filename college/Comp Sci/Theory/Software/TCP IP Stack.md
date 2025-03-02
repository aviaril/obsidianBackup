Protocol - set of rules for communicating between computers 
protocol layering - d
protocols into separate layers to perform a specific function. 

Protocol layering allows for a more modular design and simplifies troubleshooting. 
# Layers of the stack 
## Application 
- Interacts directly with software applications 
- Prepares data for transmission over the network (a process called encapsulation)
- encrypts/decrypts data 
## Transport
- receives data from the application layer 
- responsible for end to end communication between source and destination 
- breaks data down into packets 
- each packet is assigned a post number 
## Internet 
- Controls flow and routing of traffic 
- Reassembles packets back into data 
- provides IP addresses for packet sources and destinations  
## Link
- Sends data from internet layer 
- transmits 