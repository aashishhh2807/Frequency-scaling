# Frequency Scaling

## Overview
This project implements **frequency scaling using digital logic**.  
Frequency scaling is used to **increase or decrease the frequency of a clock signal** depending on the required application.

In digital systems and FPGA designs, frequency scaling is commonly used for:
- Clock division
- Clock multiplication
- Power optimization
- Timing control in digital circuits

This project demonstrates how a **higher frequency clock can be scaled to generate a lower frequency clock signal** using counters and sequential logic.

---

## Features
- Frequency division using digital counters
- Stable output clock generation
- Simple and synthesizable Verilog design
- Suitable for FPGA implementation
- Useful for timing control in digital systems

---

## Working Principle
Frequency scaling works by **counting clock cycles of the input clock** and toggling the output clock after a predefined count value.

Example:

If the input clock is **100 MHz** and the counter divides it by **10**, the output frequency becomes:

Output Frequency = Input Frequency / Division Factor
