The project is an alarm clock using the PIC's internal RC circuit to keep time, this is inaccurate but easier than clocking externally. 

---
The user sets the Alarm then the current time at the beginning of the program, button7 will be so that I can use bit 7 for the piezo with 6 being used to increment the selected digit, 5 being use to change the selected digit and 4 being used to move the program to the next stage.
Digit One refers to the rightmost digit of the displays
<span style="color:rgb(0, 176, 240)">piezo is on bit 7 Port B</span>

piezo should be 500hz 100-120 bpm
# Testing Logs
Starting 14/05/24
### Display
	1. 09:20 display subroutine written but does not give an output, presumed cause to be the digits incrementing past nine too quickly.
	2. 10:32 display still has no output, display routine found to be at fault
	3. 10:42 display Subroutine re-written, still no output
17/05/24
	1. 11:49 display Subroutine re-written, still no output.
	2. 11:56 moved display code to main program for testing, no output but the external interrupt light now shows on displays 1 and 4 instead of just display 4, not sure why this happens.
	3. 12:00 disabled external interrupt, light now only shows on display 4.
	4. 13:21 after re-writing the display subroutine it gives no output but the external interrupt light now moves between displays.
	5. 13:29 - After clearing the digits before they are set nothing has changed
21/05/24
   1. 09:31 - replaced the look-up table with test code to turn on all LEDs, upon running only displays 1 and 3 were lit.
   2. 09:36 - set Current display to 4 at the start of the program, once run displays 3 and 4 displayed an 8 (equivalent to b'01s111111') despite being set to b'11111111'
   3. 09:51 - after reverting changes from a test only display four has an output.
   4. 09:58 - all displays now work, however the wrong numbers are displayed, 1011 instead of 4321.
   5. 10:04 - all displays now give an output.
   6. 10:40 - added code to increment numbers before they are displayed, this broke everything
   7. 11:06 - changed code to display four fives and then increment them, the fives display but do not increment
   8. 11:11 - added argument to "incf", this has changed nothing
   9. 11:17 - changed program to manually change the digits, this has changed nothing, the PIC loves the number 5.
24/05/24
	1. 12:16 - changed display subroutine, now all displays light up and display a digit properly but the digit does not change between 
	2. 12:29 - changed display subroutine, display now works

### Clock
04/06/24
	1. 10:15 - Digit 1 now increments correctly 
	2. 10:30 - Digit 1 increments but the rest do not
	3. 10:40 - All digits now increment, but this can inly display 20 hours of 24 
	4. 11:21 - code to determine when digit 3 should increment does not work :(, should increment digit3 to 10 until digit4 is 2 and then clear both when digit3 is 4.
11/06/24
	1. 09:47 - Digit4 now resets at 2, all other digits working correctly 
	2. 09:52 - All digits function correctly 
	3. 
### Input
11/06/24
	1. 11:20 Select code is unresponsive, just displays all zeroes 
14/06/24
	1. 11:42 - Program starts by displaying all zeroes (this is intended), but no way of showing the selected digit. When button 6 is pressed a seemingly random display shows a seemingly random number and all other displays turn off. The start button does work however.
	2. 12:03 - Pressing button6 now always displays zero on display4
	3. 12:20 - Button6 now increments the digits but is polled far too quickly, button5 does not do anything.
	4. 12:26 - After re-writing the selected display logic there has been no change.
	5. 13:19 - After changing the select display subroutine to decrement the selected display Button5 still does not work.
	6. 13:30 - Button5 now changes the display just too quickly, Digits1 and 3 can also be incremented to ten, represented by a zero with a decimal point
	7. 13:51 - after debouncing the buttons they no-longer work.
18/06/24
	1. 09:21 - buttons five and six are now debounced and increment digits at an acceptable rate
	2. 09:25 - In input mode only display4 is on and clock mode flickers with display4 being significantly brighter than the rest.
	3. 09:57 - incrementing digits no-longer works and the decimal point is not removed when the display is no longer selected, the clock mode works again.
	4. 10:06 - decimal point now deactivates until digit1 when the displays break.
	5. 10:42 - decimal point now functions as intended however incrementing a digit leaves it on zero and deactivates all other digits.
	6. 11:04 - if you change the selected digit after incrementing the display breaks.
	7. 11:10 - if digit2 is selected clock mode is activated prematurely 
	8. 11:17 - you can now change the selected digits as intended but if the display is selected after the digit is incremented the display breaks
21/06/24
	1. 12:00 - can now change digit after incrementing but if the timer is started after a digit is incremented the display breaks.
	2. 12:07 - The timer will now start with incremented digits but all displays will quickly turn off, when changing the selected digit in input mode if you loop the selected digit back to the start display4 will flicker then dim instead of enabling the decimal point, if the display is incremented again displays 4 and 3 will have the decimal point while dispaly4 is still noticeably dimmer than the rest, if the selected digit is looped again all displays will turn off and the program will become unresponsive.
	3. 13:34 - can now loop the selected digit as intended but if the timer is started digit4 will be changed to a dimmer copy of digit3 and the display will break when it rolls over, if digit2 is incremented the display will break when it tries to roll-over and if digit1 is incremented all displays will turn off when it tris to roll over.
	4. 13:43 - The Time set function seems to be working as intended
	5. 
# Change Logs
- 17/05/24
	- 10:01 - Re-Written selection logic of the display sub-routine so that it now uses the zero bit instead of the decfsz command.
	- 10:34 - Added notation to display subroutine.
	- 11:43 - commas are illegal characters.
	- 13:18 - Re written display subroutine so that it no longer copies CurrentDisplay to another file register.
	- 13:48 - set prescaler to 1:32
- 21/05/24
	- 09:13 - changed "movf PORTB" to "movwf PORTB" in the display subroutine
	- 09:40 - changed prescaler to 1:64 
	- 09:51 - reverted changes from a test that meant the timer interrupt was not calling display
	- 09:56 - removed the code to set CurrentDisplay to 4 from the main loop, now happens before the main loop so that all displays are used
- 24/05/24
	- 09:21 - added return commands to subdisplay4 and the main display subroutine.
- 03/06/24
	- 13:33 - added code to increment digit 1
- 04/06/24
	- 10:17 - added code to increment digits 2 - 4
	- 10:39 - fixed code to increment all digits
	- 10:43 - added subroutine to wait a minute (Time is sped up to make testing easier)
- 11/06/24
	- 11:19 - added code to select time
- 14/06/24 
	- 11:37 - changed code to input time so that it polls PORTA instead of PORTB
	- 11:57 - called display in the input-time subroutine in an attempt to keep the displays cycling after a digit is incremented
	- 12:13 - added code to clear the digits if they are above they need to be reset, i.e. they are above the point at which they increment.
	- 12:25 - re-written code to change the selected display
	- 13:16 - code to change the selected display to decrement the current display instead of increment.
	- 13:51 - debounced switches five and six by adding wait100ms subroutines after they 
- 18/06/24
	- 09:16 - debounced switches five and six by adding wait100ms subroutines before functions of the buttons are executed
	- 09:24 - added code to show which display is selected
	- 11:04 - added code to remove decimal point when entering clock mode
- 21/06/24
	- 11:55 - changed sublw to subwf to stop negative numbers being fed into the digit table and breaking the display
	- 14:06 - fixed time set subroutine and added alarm set subroutine,
- 28/06/24
	- 09:44 - Fixed spelling mistakes in "GetAlarm" that were causing errors, fixed spelling mistakes in "Compare" that were causing errors, compare now calls buzz when all digits are the same as the alarm digits.
- 08/07/24
	- 12:16 added a subroutine to display alarm digits, now will not enter clock mode
# Plans/ To Do
- [x] Finally Finish Display
- [x] Add clock functionality
- [ ] Take input from user
- [ ] Make alarm sound
#### 24 hour time pseudocode 
	pseudocode for incrementing digit4 at the correct time
increment dig1 to 10
increment dig2 to 6
if dig4 < 2{
increment dig3 to 10
}else increment dig3 to 4
increment dig4 to 2


## Write-up
