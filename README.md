# Beyond-Bits

## Introduction:
Creating an analog calculator that utilizes electrical voltages is an impressive feat that blends the principles of analog computing with modern electrical engineering. This type of calculator leverages varying voltage levels to represent and manipulate numerical values, performing calculations through analog circuits. By using components such as resistors, capacitors, and operational amplifiers, the device can execute arithmetic operations like addition, subtraction, multiplication, and power. The continuous nature of voltage signals allows for smooth and precise calculations, offering a unique perspective on problem-solving compared to digital calculators. 

Analog computing is notably faster for certain types of computations because it processes data in parallel rather than sequentially. This parallelism allows for instantaneous calculation of complex mathematical functions, making analog calculators particularly effective for real-time applications and dynamic simulations.
## Methodology:
First of all in order to solve the arithmetic expression using BODMAS rule we must first convert the expression to postfix expression. This is done using Arduino. For ex: a*b+c will be converted to ab*c+. Now Arduino reads the first two operands and outputs the appropiate voltage levels, while choosing the next following operator depending on which the operation is selected on the analog MUX (IC CD74HC4051). Now Arduino reads this answer and the next following number followed by the corresponding symbol depending on which the operator is selected again, and this cycle continues till there is no operand left.

The input to the Arduino is given by a smartphone which is connected to the Arduino board via Bluetooth using the HC-05 module. We must note that Arduino does not give fixed DC voltages (except for 5V), it gives a PWM signal of frequency 490Hz with it's average voltage equal to the desired DC voltage. To solve this issue we have just added a simple RC filter to make it an approximate DC voltage. To operate upto a range of 12V we have to scale the values appropriately hence, we have connected the arduino output to an Op-amp that will increase the value by 2.4 times because Arduino can only ouptut a maximum of 5V, and similarly before the Arduino reads the value the voltage is scaled down by 2.4 times to protect the Arduino from excess voltage because Arduino cannot read more than 5V, again this is done using Op-amps. 
## Project Veterans:
1) VENU MADHAV P L
2) SHASHWAT SHARMA
3) VIBHANSHU
