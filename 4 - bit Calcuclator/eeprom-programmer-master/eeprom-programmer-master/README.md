# Arduino EEPROM programmer

This code and schematic are [MIT licensed](http://en.wikipedia.org/wiki/MIT_License).

## Circuit

This is a simple circuit for programming the 28C16, 28C64, 28C256, and similar parallel EEPROMs using an Arduino. Since the Arduino doesn’t have enough pins to directly control all of the address, data, and control lines of the EEPROM, two 74HC595 shift registers are used for the 11 address lines (15 for the 28C256) and the output enable control line.

![Schematic of EEPROM programmer](https://raw.githubusercontent.com/beneater/eeprom-programmer/master/schematic.png)

### 1. Basic programmer

The code in [`/eeprom-programmer`](/eeprom-programmer) is the basic programmer that programs a few bytes into the EEPROM and dumps the contents.

That software, along with the EEPROM programmer’s hardware are described in detail in the following video. This is a good place to start if you’re looking for the fastest way to make sense of this repo:
- [Build an Arduino EEPROM programmer](https://youtu.be/K88pgWhEb1M).

### 2. 8-bit decimal display

The code in [`/multiplexed-display`](/multiplexed-display) is for programming an EEPROM to be used to decode 8-bit values and drive a 4-digit 7-segment display. Check out this video for more:
- [Build an 8-bit decimal display for our 8-bit computer](https://youtu.be/dLh1n2dErzE).

