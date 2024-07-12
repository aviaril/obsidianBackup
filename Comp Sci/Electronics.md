# Introduction
An alarm clock can be a vital part of some people's working lives guaranteeing that they do not sleep in, alternatively they can be used to ensure the user is not late for whatever they are doing that day be that getting a train or meeting a deadline.
Alarm clocks can help in these aspects by acting as notifications that it is a certain time telling the user what they had to do, i.e. The alarm goes off at 07:00 telling the user that it is time to get out of bed or the alarm goes off ten minuets before they have to leave for the train, reminding them that they have ten minuets to finish getting ready and leave. Such uses can allow a person to be more productive. 

---
# Specification

## User Guide

After powering the system the user will be prompted to input the time they would like the alarm to go off, they can do this by using the leftmost button (Button6) select a digit, the currently selected digit is indicated by the decimal point. The user can then increment the selected digits as necessary using the middle button (Button5), after the user has set their desired alarm they can confirm their input by pressing the rightmost button (Button4), this will move them onto the next portion of the program setting the current time. The user will set the current time by using the same controls mentioned above, after the current time is set the user can 
##   
---
The clock runs off a +5-0Volt power supply counts in one second increments on four multiplexed seven-segment displays that display one of 20 digits, the first ten are human readable numbers 0-9 and the last ten are the same digits only with the decimal point of the displays active, the decimal point is used to show which display is currently selected when the circuit is taking an input form the user.

The first digit is incremented every minute, once this reaches ten it resets to zero and the second digit is incremented, once the second digit is incremented to six it resets to zero and increments to 0. The Third digit will reset and increment the fourth once it reaches ten if the fourth digit is zero or one however if the Fourth digit is two the third will rollover at five, this prevents the clock from displaying illegal times such as 27:00 while still allowing it to display legal times where the Third digit is over four such as 17:00. 

Theoretically the active display switches every 576ms as set by a precale of 1:32 and an operating clock speed of 8MHz, this results in a visually smooth display that doesn't flicker . The clock operates on 24 hour time meaning it counts to 2400 before resetting to 0000. 

The three buttons connected to bits 4-6 of port A are debounced through the software running on the PIC instead of though a physical circuit, this is done by making the program wait for 200ms before executing the code attached to that input. The buttons are debounced this way because it is easier to build and design to produce the same effect, as a secondary benefit it also reduces the material cost of the circuit as there is no need for a dedicated RC circuit or any other hardware solutions.


---
# Limitations 
The displays cannot be photographed with a standard shutter speed and most video will show the displays cycling meaning that it is hard to read the output from a video. 