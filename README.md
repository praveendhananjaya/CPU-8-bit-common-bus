# CPU-8-bit-common-bus (SAP-1 Processor Architecture) 

A simple 8-bit micro-processor using mostly discrete logic chips.

![alt text](https://github.com/praveendhananjaya/CPU-8-bit-common-bus/blob/main/doc/test.gif?raw=true)

![alt text](https://github.com/praveendhananjaya/CPU-8-bit-common-bus/blob/main/doc/SAP1.jpeg?raw=true)


## Submodules:

- Clock with adjustable frequency and single-step button
- 2 8-bit Data Registers (A & B)
- ALU implementing sum and difference between Registers A & B, carry and zero flag
- Flag Register to save the ALU flags between instructions
- 4-bit Instruction Counter with load (jump)
- Output module to display a byte as positive decimal or 2s-complement with data latch
- Random Access Memory with 16 Bytes for instructions and data
- 4-bit Memory Address Register to address the 16 bytes of RAM
- 8-bit Instruction Register with the upper nibble representing the opcode, the lower nibble can be used for instruction parameters
- Instruction Decoder to run the microcode of the 16 different instructions with 5 microinstuctions each. Uses a 16-bit control word to control the other modules


schematic diagram

![alt text](https://github.com/praveendhananjaya/CPU-8-bit-common-bus/blob/main/doc/Schematic_8BitComputer_2021-05-04.png?raw=true)
