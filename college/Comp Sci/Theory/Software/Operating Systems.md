
Types of Operating System
--
---

**Distributed**
A distributed operating system is a collection of independent networked nodes. Each node may have it's own hardware associated to it, there will be system management software that brings the interconnected systems together that coordinate individual and collaborative activities on different nodes.

**Embedded** 
An Embedded operating system has a dedicated function and can be part of a larger device, they generally have a  lower power consumption, lower cost and use limited hardware resources meaning they have to be interfaces with in a bespoke way e.g. the operating system on a smart device will likely be embedded.  

**Multi-Tasking** operating systems are those that allow you to run many separate tasks at once, this is now standard among most operating systems, however in some fields tasks can require far more processing power than a normal computer can feasibly provide, in this case a supercomputer may be used. In order to keep costs down the operating system may designed as a multi-user system so that several users can send tasks to it and share system resources.

**Multi-User** operating systems allow many different users to use the computer's resources simultaneously, these systems share processor time and have little processing done at the terminals e.g. Automated tills at a supermarket.

**Real-Time** operating systems run under predefined deadlines and can be classed as time-critical, these systems operate under the principal that the right answer too late is wrong, Soft Real-Time OS can generally complete a task within a deadline while a Hard Real-time OS will meet the deadline unless a problem with the hardware arises.  Real-time OS are event-driven meaning that they switch between tasks based on the task priority rather than clock interrupts. This type of system can be seen in plane control systems or medical equipment.

**Network** operating systems allow users to share resources and data with the terminals having their own processing capability and software, they also have security features that allow different people to access different parts of the network.
**Memory**
--
---

-RAM and ROM
memory management ensures RAM is unused efficiently, removes data that is not needed(garbage collection)
virtual memory may be used when RAM is almost full to allow 
***Paging***
pages are fixed sized physical divisions
programs are split into a given number of pages 
paging takes no account of how splits a program 
can separate instructions inside a looping condition so they are in different pages, this is inefficient so those instructions should be kept together
***Segmentation***
-segments are logical divisions with different sizes 
-complete segment of a program
-this allows a program to be split into multiple smaller segments meaning it can be run under more situations
***Virtual Memory***
-some instructions that are not likely to be called soon can be moved to virtual memory in secondary storage.

***Advantages***
Frees space in RAM allowing it to be used more efficiently 

## Scheduling##

---
**Processes**
*Process*- A program loaded into memory that can be executed by the CPU
- Processes are given access to system resources, for example processor time which enables multi-tasking
- Each process has a small area of data called the *Process Control Block* (PCB)  located in the data segment of the system's kernel, this provides the CPU Scheduler with the detail needed to manage the process e.g. the priority of the process, the processing time used, if it needs other resources 
- If a process is awaiting an input it can be moved to the waiting queue to not waste CPU time that could be used on other processes, when the peripheral sends the data it issues an interrupt to the CPU to run the process removing it from the waiting queue and executing it.
- Deadlock is the term used to describe an undesirable situation where processes are not running because they are waiting on each other to do something e.g. Process 1 has a file open and is trying to print it but cannot because Process 2 is using the printer and trying to open the same file to print but cannot as Process 1 already has the file open. The scheduler can deal with this in many way such as not allowing a process to run until all recourses it needs are available, or allocating recourses in the same order. If a deadlock is detected (usually by the processes sitting in the wait queue for too long) the operating system will remove one of the processes.

**Uses of Scheduling**
- Makes maximum use of CPU time
- Makes the computer more responsive to the user 
- Gives the ability to prioritise jobs 
- Ensures no process is starved of processor time
- Allows more processes to run simultaneously
- 
**Types of Scheduling**
- *Round Robin* allocates a fixed time for a process to be executed and then cycles through them until they are complete. Processes are ordered in a First In First Out list, this is good as it distributes the processor time well but a downside id that it takes no account of priority.
- *Priority Scheduling* compares the relative priorities of processes and then executes the process with the highest priority, this means that the most urgent jobs get done first but low priority jobs can take longer to run or never get run because of this, this is fixed by increasing the priority of lower jobs to ensure that they will be run.
- *Shortest Burst* will prioritise the process with the shortest burst of CPU time, this allows the CPU to process more jobs but if jobs have similar burst times t becomes inefficient  
- *First Come First Served* simply places processes in a queue and executes them in order
- *Multi-level feedback queues* categorise processes into their ow queues, different queues can have different prioritisation algorithms, e.g. user and system processes may have different queues
- *Shortest Job First* executes smaller processes before larger ones to get them out of the way
- *Shortest Remaining Time* is similar to Shortest job first but it interrupts the current process instead of queuing it next
- 
---


BIOS
--
---
**uses of the BIOS**
- Runs the Bootloader, the program that places the system kernel into memory
- Can configure the order of drives the computer will attempt to boot from
- Performs a Power-on-Self-Test (POST) to ensure all components are functioning correctly 
- Activates other BIOS chips on the computer for e.g. graphics cards and other components can have their own BIOS chips 
- Providing low-level routines such as managing the display and keyboard
---
