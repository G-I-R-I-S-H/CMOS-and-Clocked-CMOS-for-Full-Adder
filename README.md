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
# Creating a Full Adder Design in Cadence Virtuoso (UMC_180nm)

Follow these steps to create your **own library**, build the schematic, and prepare for simulation in **Cadence Virtuoso**.

---

## Create a New Library
- Open Virtuoso CIW.  
- Go to: `File → New → Library`  
- Enter:  
  - **Library Name**: `FULL_ADDER_CMOS`  
- Select:  
  - **Attach to an existing technology library**  
  - Choose **`UMC_180nm`**  
- Click **OK**.  
✅ Your custom library is now linked to the UMC 180nm technology.

---

## Create a Cell View
- Go to: `File → New → Cell View`  
- Fill in the details:  
  - **Library**: `FULL_ADDER_CMOS`  
  - **Cell Name**: `full_adder_schematic`  
  - **View Name**: `schematic`  
  - **Tool**: `Schematic Editor`  
- Click **OK** to open the schematic editor.

---

## Place PMOS and NMOS Devices
- Open the **Add Instance** dialog:  
  - Shortcut: Press **`i`**  
- From the **UMC_180nm PDK library**:  
  - Select **PMOS** for p-channel transistors.  
  - Select **NMOS** for n-channel transistors.  
- Place the devices as per your **Full Adder design**:  
  - Build XOR, AND, and OR gates.  
  - Connect:  
    - **VDD** to PMOS sources.  
    - **GND** to NMOS sources.  
    - Input/Output pins for `A`, `B`, `Cin`, `Sum`, and `Carry`.

---

## Save and Check
- Save the schematic: **Ctrl + S**  
- Go to: `Design → Check and Save`  
- Ensure there are **no errors or warnings**.

---

Similarly create for the Clocked CMOS Logic.
## Simulation Using ADE L
- Open **ADE L** (Analog Design Environment - L) from Virtuoso.  
- Load the **schematic cell view** for either:
  - `full_adder_cmos`
  - `full_adder_clocked_cmos`
- Set the **VDD** source to **1.8 V**.  
- Go to `Analysis → Choose` and select:
  - **Type**: `Transient (tran)`  
  - **Run Time**: `100 ns`
- Apply input stimulus signals (e.g., `vpulse` sources for A, B, Cin, and clock in the clocked design).  
- Run the simulation and observe the waveforms for:
  - `Sum`
  - `Carry`

---
## Fully CMOS Logic

The schematic of the **Fully CMOS-based Full Adder** is shown below, where the circuit is implemented using static CMOS logic gates such as XOR, AND, and OR to achieve the desired sum and carry outputs.

![Fully CMOS Full Adder Schematic](/Results/Results_CMOS/Fully_CMOS.jpg)

The simulation results for the **Fully CMOS design** are provided below, clearly demonstrating the correct generation of sum and carry signals for all possible input combinations, validating the functional correctness of the design.

![Fully CMOS Full Adder Simulation](/Results/Results_CMOS/Fully_sim.jpg)

## Clocked CMOS Logic

The **Clocked CMOS Full Adder** schematic is implemented in Cadence Virtuoso using the UMC 180nm technology library. This design incorporates a clock input to optimize the operation of the circuit and improve performance in specific applications. The schematic diagram is shown below:

![Clocked CMOS Full Adder Schematic](/Results/Results_CMOS/Clocked_CMOS.jpg)

The corresponding **output simulation** demonstrates the correct operation of the Clocked CMOS Full Adder for all possible input conditions, as illustrated below:

![Clocked CMOS Full Adder Simulation](/Results/Results_CMOS/Clocked_simulation.jpg)



