# CMOS-and-Clocked-CMOS-for-Full-Adder
Design and analysis of CMOS and Clocked CMOS logic for implementing a full adder. Includes transistor-level design, simulation, and performance comparison to evaluate power, delay, and area efficiency for digital circuit applications.

## Full Adder
A **Full Adder** is a fundamental digital circuit that performs binary addition of three input bits — two significant bits (*A* and *B*) and a carry-in (*Cin*) — producing a **Sum** and a **Carry** output.

This project implements the Full Adder using two approaches:

- **Fully CMOS Logic Network** – Implements the logic using static CMOS design for stable performance.  
- **Clocked CMOS Logic Network** – Utilizes clocked transistors to optimize performance for specific applications.  

## Features
- Design and simulation of the **circuit diagram** and **truth table**.  
- **Performance analysis** of power consumption and propagation delay.  
- Validation of the design with simulation outputs. 

## Methodology: Full Adder Design in Cadence Virtuoso

This guide explains the step-by-step procedure to design and analyze a **Full Adder** using **Fully CMOS** and **Clocked CMOS logic** in **Cadence Virtuoso**.

---

### 1️⃣ Start the Cadence Environment
Open the Terminal
```bash
tcsh
```
### 2️⃣ Source the Cadence Environment
```bash
source cshrc
```
### 3️⃣ Open Virstuoso
```bash
virtuoso &
```