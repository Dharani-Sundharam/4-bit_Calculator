# 4-Bit Calculator using Logic Gates, EEPROM

## Overview
This project is a 4-bit calculator built on a breadboard using basic electronic components like logic gates, EEPROM, seven-segment displays, and flip-flops. The calculator performs addition, subtraction, and multiplication, with all computations handled by hardware logic. The Arduino is only used as a power source for the circuit.

The main inspiration for this project was [4 bit calculator](https://youtu.be/dkWq9me-BgA?si=M9wrhzlmyDGgSlWt) video by Oskar Fornander

And also Ben Eater's [8-bit breadboard computer](https://youtu.be/HyznrdDSSGM?si=EtFizgErSCoZNm4c) (You should defnitely watch the full playlist !!!)

## Components Used
- Breadboard
- **Arduino (only for power supply)**
- Logic gates (AND, OR, NOT, XOR) and a CD4511 IC [Datasheet](https://www.alldatasheet.com/datasheet-pdf/pdf/26905/TI/CD4511.html)
- EEPROM (for BCD storage) (I used the 28C16 EEPROM. [Datasheet](http://cva.stanford.edu/classes/cs99s/datasheets/at28c16.pdf))
- Seven-segment displays (You can use common cathode or anode according to your availability Note: you may want to use NOT gates in order for it to function so choose your components carefully)
- JK flip-flop
- D latch
- Clock (I used a 555 timer to represent a clock)
- Resistors, capacitors, and LEDs (resistors and capacitors are variable refer Ben eater's Video for more information)
- Push buttons for user input

## Circuit Design
The calculator is designed with a series of logic gates to handle arithmetic operations. 
- **Addition**: Handled through binary logic.
- **Subtraction**: Performed using 1's complement method.
- **Multiplication**: Implemented through a combination of logical operations.
- **Memory Storage**: EEPROM is used to store and retrieve BCD numbers.(To program this EEPROM refer this [Video](https://youtu.be/K88pgWhEb1M?si=GXDwM58lp-yxiVb2))
- **Display**: Results are shown on seven-segment displays.(Displays are multiplexed together refer this [Video](https://youtu.be/dLh1n2dErzE?si=hw1QeJVOJbqLBQao))

The Arduino supplies 5V power to the circuit, and all logic control happens through the breadboard components.

## Working Principle
### Addition
Addition is achieved by binary logic implemented through a Full-adder IC [74LS283]

### Subtraction (1's Complement Method)
Subtraction is implemented using the 1's complement method with a toggle switch to flip between addition and subtraction modes.

### Multiplication
Binary multiplication is done through logical combinations of inputs, which are processed by the gates and displayed in BCD format.

**Circuit I used for multiplication**:
![Traditional-4-bit-array-multiplier](https://github.com/user-attachments/assets/7d9c86fc-47e0-4861-ad7a-ed15b1f6890b)


## Challenges Faced
- Debugging the circuit to ensure proper functionality of all arithmetic operations.
- Ensuring the correct BCD display of results on the seven-segment display.
- Handling binary overflow in addition and subtraction.

## Future Improvements
- Adding division functionality to complete the set of basic arithmetic operations.
- Optimizing the design to handle more complex operations or a higher bit-length (e.g., 8-bit or 16-bit).
- Improving efficiency by minimizing power consumption.

## Setup Instructions
1. **Assemble the Circuit**:
   - Follow the schematic diagram to connect the logic gates, EEPROM, flip-flops, and displays on the breadboard.
  
   - **The binary to decimal seven segment display control logic**:
  
   ![BCD proto 2](https://github.com/user-attachments/assets/e84604e3-5ea1-4e06-991e-9eb340a8af4a)


![4 - bit to BCD with counter](https://github.com/user-attachments/assets/cc565543-cdef-47cb-8f7c-a0e92d4b47ce)


   - Connect the Arduino to provide a 5V power supply.

3. **Using the Calculator**:
   - Use the push buttons to input numbers.
   - Toggle the switch to select between addition and multiplication modes.
   - View the results on the seven-segment display.

## Project Images and Circuit Diagrams

**The Addition function**:
![Addition](https://github.com/user-attachments/assets/ae884162-e764-48e9-bb62-afd367c3786c)

**The Multiplication function**:
![Multiplication](https://github.com/user-attachments/assets/d9ab3b01-452f-4fe4-99fc-88df4be5664e)

**The Full calculator function**:
![Full image](https://github.com/user-attachments/assets/31fcb14f-fa15-4c83-ae7d-1809e649d48b)

## For more information:

**Tinkercad link**:
Will be available soon !!!

**Refer the files in the repository and read the PDF**

[4BBC_documentation.pdf](https://github.com/user-attachments/files/17177556/4BBC_documentation.pdf) *Credits: Oskar Fornander*

## All the Codes I used are in the '4 - bit Calcuclator/eeprom-programmer-master/eeprom-programmer-master' refer the repository and this [video](https://youtu.be/K88pgWhEb1M?si=3_O_zjXV89EgjO-n)

## License
This project is licensed under the MIT License.

