# sky130A
CMOS Inverter Design and Physical Verification using SKY130A

# CMOS Inverter Design and Simulation Using SKY130A

<p align="center">
  <b>CMOS Design | Open-Source EDA | SKY130A Technology</b>
</p>

## 1. Introduction

CMOS (Complementary Metal-Oxide-Semiconductor) technology is widely used in modern integrated circuit design due to its low power consumption and high efficiency.

This project demonstrates the design and pre-layout simulation of a CMOS Inverter using the SKY130A open-source Process Design Kit (PDK).

The main focus is to understand the CMOS inverter structure, develop its schematic, perform circuit simulation, and analyze the corresponding input and output waveforms.

## 2. Project Objectives

- Understand the basic operation of a CMOS inverter.
- Design the inverter schematic using Xschem.
- Configure the SKY130A technology environment.
- Perform transient simulation using NGSpice.
- Analyze the input and output voltage waveforms.
- Gain practical experience with open-source VLSI design tools.

## 3. Tools and Technologies

| Tool | Application |
|---|---|
| Ubuntu (WSL2) | Linux environment |
| SKY130A PDK | Process Design Kit |
| Xschem | Schematic design |
| NGSpice | Circuit simulation |
| Magic VLSI | Physical layout |
| Netgen | LVS verification |

## 4. CMOS Inverter Architecture

A CMOS inverter consists of two MOS transistors:

- PMOS transistor – Pull-up network.
- NMOS transistor – Pull-down network.

Both transistors operate complementarily to produce an inverted output.

### Truth Table

| Input (Vin) | Output (Vout) |
|---|---|
| 0 (LOW) | 1 (HIGH) |
| 1 (HIGH) | 0 (LOW) |

## 5. Design and Simulation Flow

The following stages are included in the current project:

1. EDA tool installation and configuration.
2. SKY130A PDK setup.
3. CMOS inverter schematic development using Xschem.
4. SPICE netlist and testbench preparation.
5. Transient simulation using NGSpice.
6. Input and output waveform analysis.

## 6. Schematic Design

The CMOS inverter schematic was developed using Xschem with the SKY130A technology library.

The schematic represents the complementary PMOS and NMOS transistor configuration.

![CMOS Inverter Schematic](images/01_schematic.png)

## 7. Circuit Simulation

Pre-layout simulation was performed using NGSpice to study the switching behaviour of the CMOS inverter.

The transient analysis helps evaluate the relationship between the input and output signals.

![NGSpice Simulation](images/02_simulation.png)

## 8. Waveform Analysis

The input and output voltage waveforms are observed to verify the inverter functionality.

Expected behaviour:

- LOW input produces HIGH output.
- HIGH input produces LOW output.
- The output follows the logical complement of the input.

![Input and Output Waveforms](images/03_waveform.png)

## 9. Current Project Status

**Completed:**
- EDA environment setup.
- SKY130A PDK configuration.
- CMOS inverter schematic design.
- SPICE simulation.
- Waveform generation and analysis.

**Upcoming Work:**
- Physical layout development using Magic.
- Design Rule Check (DRC).
- Layout Versus Schematic (LVS).
- Parasitic extraction.
- Post-layout simulation.

## 10. Learning Outcomes

- Practical understanding of CMOS inverter operation.
- Experience with Xschem and NGSpice.
- Familiarity with SKY130A technology.
- Understanding of the schematic-to-simulation workflow.
- Introduction to VLSI physical verification.

## 11. Author

**G. Pravallika**  
B.Tech – Electronics and Communication Engineering

*This is an ongoing learning project. Further physical design and verification stages will be documented as they are completed.*
