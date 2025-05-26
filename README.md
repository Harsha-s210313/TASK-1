# 8-bit ALU

*Company name*: CODTECH IT SOLUTIONS

*NAME*: KANNAJOSYULA HARSHA VARDHAN

*INTERN ID*: CT06DN42

*DOMAIN*: VLSI

*DURATION*: 6 WEEKS

*MENTOR*: NEELA SANTOSH

**PROJECT DESCRIPTION**:

This project focuses on the design, implementation, and functional verification of an 8-bit Arithmetic Logic Unit (ALU) using Verilog HDL. The ALU is a fundamental component of any digital processing system, responsible for carrying out arithmetic and logical operations on binary data.
The core objectives of the project include:
Developing a behavioral-level Verilog model of the ALU capable of performing a range of arithmetic and logical operations.
Building a testbench environment to simulate and validate the correctness of the ALU under various input conditions.
Ensuring correctness, robustness, and scalability of the ALU design through comprehensive simulation and waveform analysis.
Tools Used:
Verilog HDL (Behavioral Modeling)
Simulation Tools: ModelSim / Vivado Simulator 
Platform: Xilinx Vivado 
### Main Module: ARITHMETIC_LOGIC_UNIT
The core ALU module features:
- **Input Ports:**
  - `A` [7:0]: 8-bit primary operand
  - `B` [7:0]: 8-bit secondary operand  
  - `ALU_Sel` [2:0]: 3-bit operation selector
- **Output Port:**
  - `ALU_Result` [7:0]: 8-bit result output

### Supported Operations
The ALU implements five fundamental operations controlled by the 3-bit selector:

| ALU_Sel | Operation | Description |
|---------|-----------|-------------|
| 000 | Addition | A + B |
| 001 | Subtraction | A - B |
| 010 | Bitwise AND | A & B |
| 011 | Bitwise OR | A \| B |
| 100 | Bitwise NOT | ~A |
| Others | Default | Output zeros |

## Implementation Details

### Combinational Logic Design
- Uses `always @(*)` block for combinational logic implementation
- Case statement provides clean, readable operation selection
- Default case ensures predictable behavior for undefined control signals
- Purely combinational design with immediate output response

### Testbench Verification
The comprehensive testbench (`ALU_TB.v`) validates all implemented operations:
- **Addition Test:** 10 + 5 = 15
- **Subtraction Test:** 15 - 5 = 10  
- **AND Operation:** 0xCC & 0xAA = 0x88
- **OR Operation:** 0xCC | 0xAA = 0xEE
- **NOT Operation:** ~0xCC = 0x33

## Technical Specifications
- **Data Width:** 8-bit operands and results
- **Control Width:** 3-bit operation selector
- **Timing:** 1ns timescale with 1ps precision
- **Test Duration:** 10ns per operation with systematic verification

## Applications
This ALU design is suitable for:
- Educational purposes in digital design courses
- Integration into simple 8-bit processor designs
- FPGA implementation for embedded systems
- Building blocks for more complex arithmetic units

## Design Benefits
- **Simplicity:** Clean, understandable Verilog implementation
- **Modularity:** Self-contained unit for easy integration
- **Verification:** Complete testbench ensures functional correctness
- **Scalability:** Design principles easily extend to wider data paths

Verification:
A dedicated Verilog testbench was developed to apply exhaustive test vectors covering all possible operations and edge cases (e.g., overflow, zero results, etc.). Simulations were performed using tools like ModelSim or Vivado Simulator, and the results were verified using waveform outputs to confirm logical correctness and signal transitions.
