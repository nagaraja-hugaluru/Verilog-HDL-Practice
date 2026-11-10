# 4-bit Ripple Carry Adder

## Objective
Design and implement a 4-bit Ripple Carry Adder using Structural Verilog HDL.

## Inputs
- A: 4-bit input
- B: 4-bit input
- Cin: Carry input

## Outputs
- Sum: 4-bit sum output
- Cout: Final carry output

## Architecture
The Ripple Carry Adder is constructed using four 1-bit Full Adder modules connected in series.

The carry output of each Full Adder is connected to the carry input of the next Full Adder.

## Design Methodology
- Structural Modelling
- Module Instantiation
- Cascaded Carry Propagation

## Verification
The design will be tested using a Verilog testbench with different input combinations, including carry propagation and overflow cases.

## Tools Used
- Verilog HDL
- Xilinx Vivado

## Project Files
- `full_adder.v` – 1-bit Full Adder module
- `ripple_carry_adder.v` – 4-bit Ripple Carry Adder design
- `tb_ripple_carry_adder.v` – Testbench

