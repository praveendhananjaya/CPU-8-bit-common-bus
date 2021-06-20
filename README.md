# CPU-8-bit-common-bus (SAP-1 Processor Architecture) 

A simple 8-bit micro-processor using mostly discrete logic chips. The Simple-As-Possible (SAP)-1 computer is a very basic model of a microprocessor. The SAP-1 design contains the basic necessities for a functional Microprocessor. 


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


## Program Counter
    It counts from 0000 to 1111.
    It signals the memory address of next instruction to be fetched and executed.
## Inputs and MAR (Memory Address Register)
    During a computer run, the address in PC is latched into Memory Address Register (MAR).
## The RAM
    The program code to be executed and data for SAP-1 computer is stored here.
    During a computer run, the RAM receives 4-bit addresses from MAR and a read operation is performed. Hence, the instruction or data word stored in RAM is placed on the W bus for use by some other part of the computer.
    It is asynchronous RAM, which means that the output data is available as soon as valid address and control signal are applied.
## Instruction Register
    IR contains the instruction (composed of OPCODE+ADDRESS) to be executed by SAP1 computer.
## Controller-Sequencer
    It generates the control signals for each block so that actions occur in desired sequence. CLK signal is used to synchronize the overall operation of the SAP1 computer.
    A 12-bit word comes out of the Controller-Sequencer block. This control word determines how the registers will react to the next positive CLK edge.
## Accumulator
    It is a 8-bit buffer register that stores intermediate results during a computer run.
    It is always one of the operands of ADD, SUB and OUT instructions.
## Adder/Subtractor
    It is a 2's complement adder-subtractor.
    This module is asynchronous (unclocked), which means that its contents can change as soon as the input words change.
## B-register
    It is 8-bit buffer register which is primarily used to hold the other operand (one operand is always accumulator) of mathematical operations.
## Output Register
    This registers hold the output of OUT instruction.
## Binary Display
    It is a row of eight LEDs to show the contents of output register.
    Binary display unit is the output device for the SAP-1 microprocessor.

schematic diagram

![alt text](https://github.com/praveendhananjaya/CPU-8-bit-common-bus/blob/main/doc/Schematic_8BitComputer_2021-05-04.png?raw=true)
