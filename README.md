# 8-bit Microcontroller CPU Design (VHDL)
This is a project I developed to demonstrate my understanding of processor architecture and digital design using VHDL.
The design implements a complete 8-bit CPU with ALU, Control Unit, Data Path, and Memory subsystems that can fetch, decode, and execute instructions.

# What the project does
ALU Module – Performs arithmetic (ADD, SUB) and logical (AND, OR) operations with increment/decrement support
Data Path – Manages data flow between registers (IR, MAR, PC, A, B) and ALU using multiplexers
Control Unit – Generates control signals to orchestrate instruction execution
Memory Subsystem – Integrates ROM (128x8), RAM (96x8), and memory-mapped I/O ports
Status Flags – Updates NZVC (Negative, Zero, Overflow, Carry) flags after ALU operations
Modular Design – Clean separation of components for reusability and easy testing

# Architecture Overview
Component	Description
ALU	8-bit ALU with 6 operations: ADD, SUB, AND, OR, INC, DEC
Control Unit:	FSM-based controller generating all control signals
Data Path:	Registers (IR, MAR, PC, A, B), ALU, and bus multiplexers
Memory:	ROM (program memory), RAM (data memory), 16 I/O ports

# Language and Tools Used
VHDL – RTL design and behavioral modeling
Xilinx ISE – Simulation and verification
FPGA (optional) – Synthesis target for hardware implementation

# Steps to Simulate
Using Xilinx ISE:
Create a new project in your simulator
Add all .vhd files to the project
Compile all modules (check for any dependency order)
Create a testbench to apply clock and reset signals
Run simulation and observe waveforms for register updates and ALU operations

# Status Flags
N (Negative) – Set if MSB of result is 1
Z (Zero) – Set if result is zero
V (Overflow) – Set if signed overflow occurs
C (Carry) – Set if unsigned carry/borrow occurs

# Performance
Module count: 4 core VHDL files
Registers: IR, MAR, PC, A, B, CCR
Memory: 128-byte ROM, 96-byte RAM
I/O ports: 16 memory-mapped input/output ports

# Skills Demonstrated
VHDL RTL Design – Structural and behavioral modeling
Processor Architecture – Fetch-decode-execute cycle understanding
ALU Design – Arithmetic/logic with flag generation
Register File Design – Multiplexer-based data path
Memory Hierarchy – ROM, RAM, and memory-mapped I/O
Digital Design Concepts – Synchronous logic, control signals, bus architecture
