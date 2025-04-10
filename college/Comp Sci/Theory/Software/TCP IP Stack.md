Protocol - set of rules for communicating between computers 
protocol layering - d
protocols into separate layers to perform a specific function. 

Protocol layering allows for a more modular design and simplifies troubleshooting. 
# Layers of the stack 
## Application 
- Interacts directly with software applications 
- Prepares data for transmission over the network (a process called encapsulation)
- encrypts/decrypts data 
- removes header, other non-viewable information
## Transport
- receives data from the application layer 
- responsible for end to end communication between source and destination 
- breaks data down into packets 
- each packet is assigned a post number 
- establishes communication between devices (Handshake)
- converts this data into packets 
## Internet 
- Controls flow and routing of traffic 
- Reassembles packets back into data 
- provides IP addresses for packet sources and destinations  
- 
## Link
- Receives data from internet layer 
- Adds MAC addresses to packets 
- Sends packets to other machines 
- Passes received data back up the stack 

errors can be checked with a checksum or with 