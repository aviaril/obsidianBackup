
### Diodes
:TiCircuitDiode: Silicon Diode
- used for rectification 
- The base of the triangle is the anode
- Offers around 100,000 times the resistance in reverse bias than in forward bias 
- forward bias - anode more positive than cathode 
- in forward bias current starts to flow at 0.5V and exponentially increases at 0.7V
- In reverse bias the current is negligible until the voltage reaches the Reverse Breakdown Voltage, usually over 100V
#### Applications
- Can protect against reverse polarity, where a power supply is connected the wrong way around if a diode is on the terminal connected to the positive terminal of the power supply no current will flow, protecting the circuit from damage.
- Can protect from Back EMF;
	-Back EMF is the current generated in the opposite direction of original voltage when a magnetic field of a solenoid collapses.
	-If powering a relay with something like a MOSFET a diode should be connected between the live rail and the drain of the MOSFET in reverse bias