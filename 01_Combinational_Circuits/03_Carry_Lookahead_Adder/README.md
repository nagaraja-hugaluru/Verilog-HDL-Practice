# 4-bit Carry Look-Ahead Adder (CLA)

## 1. Project Overview
This project implements a 4-bit Carry Look-Ahead Adder (CLA) using Verilog HDL.

A Carry Look-Ahead Adder is a fast adder circuit that reduces carry propagation delay by calculating carry signals in advance using Generate and Propagate signals.

## 2. Tools Used
- Verilog HDL
- Xilinx Vivado
- Vivado Simulator (XSim)

## 3. Working Principle

The CLA uses two important signals:

- **Generate (G):** Indicates whether a bit generates a carry.
- **Propagate (P):** Indicates whether a bit propagates an incoming carry.

### Equations

**Propagate:**
```verilog
P = A ^ B;
```

**Generate:**
```verilog
G = A & B;
```

**Carry equations:**
```text
C1 = G0 + P0Cin

C2 = G1 + P1G0 + P1P0Cin

C3 = G2 + P2G1 + P2P1G0 + P2P1P0Cin

C4 = G3 + P3G2 + P3P2G1
     + P3P2P1G0 + P3P2P1P0Cin
```

**Sum:**
```text
Sum[0] = P0 ^ Cin
Sum[1] = P1 ^ C1
Sum[2] = P2 ^ C2
Sum[3] = P3 ^ C3
```

**Final Carry:**
```text
Cout = C4
```

## 4. Project Files

| File | Description |
|---|---|
| `cla.v` | Verilog design implementation |
| `cla_tb.v` | Testbench for simulation |
| `simulation_waveform.png` | Simulation output waveform |

## 5. Verification

The design was simulated using Vivado Simulator (XSim).

Different input combinations of A, B, and Cin were applied to verify the Sum and Cout outputs.

The simulation results matched the expected binary addition results.

## 6. Learning Outcomes
- Understanding Generate and Propagate signals.
- Learning Carry Look-Ahead logic.
- Implementing a 4-bit CLA using Verilog HDL.
- Writing and running a Verilog testbench.
- Verifying digital circuits using Vivado simulation.
