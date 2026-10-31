# SKY130A CMOS Inverter Design and Physical Verification

<p align="center">
  <b>CMOS Design | Open-Source EDA | SKY130A Technology</b>
</p>

## 1. Introduction

CMOS (Complementary Metal-Oxide-Semiconductor) technology is widely used in modern integrated circuit design because of its low static power consumption and high efficiency.

This project demonstrates the design, simulation, physical layout, and verification of a CMOS inverter using the open-source SkyWater SKY130A Process Design Kit (PDK). Xschem is used for schematic design, NGSpice for circuit simulation, Magic VLSI for physical layout and extraction, and Netgen for Layout Versus Schematic (LVS) verification.

## 2. Project Objectives

- Understand the operating principle of a CMOS inverter.
- Design the inverter schematic using Xschem.
- Configure the SKY130A technology environment.
- Generate and simulate the SPICE netlist using NGSpice.
- Analyze the input and output voltage waveforms.
- Create the physical layout using Magic VLSI.
- Perform Design Rule Check (DRC).
- Verify layout connectivity using LVS.
- Perform parasitic extraction and post-layout simulation.

## 3. Tools and Technologies

| Tool | Application |
|---|---|
| Ubuntu (WSL2) | Linux development environment |
| SKY130A PDK | Process Design Kit and technology files |
| Xschem | Schematic design |
| NGSpice | Circuit simulation |
| Magic VLSI | Physical layout, DRC, and extraction |
| Netgen | LVS verification |

## 4. CMOS Inverter Architecture

A CMOS inverter consists of two complementary MOS transistors:

- **PMOS transistor:** Forms the pull-up network and connects the output towards the supply voltage.
- **NMOS transistor:** Forms the pull-down network and connects the output towards ground.

The gates of both transistors are connected to the input, while their drains are connected to the output.

### Truth Table

| Input (A) | Output (Y) |
|---|---|
| LOW (0) | HIGH (1) |
| HIGH (1) | LOW (0) |

The output of a CMOS inverter is the logical complement of its input.

## 5. Design and Simulation Flow

The project follows these stages:

1. EDA tool installation and configuration.
2. SKY130A PDK setup.
3. CMOS inverter schematic development using Xschem.
4. SPICE netlist and testbench preparation.
5. Transient simulation using NGSpice.
6. Input and output waveform analysis.
7. Physical layout development using Magic VLSI.
8. Design Rule Check (DRC).
9. Layout Versus Schematic (LVS) verification.
10. Parasitic extraction and post-layout simulation.

## 6. Schematic Design Using Xschem

The CMOS inverter schematic was developed using Xschem with the SKY130A technology library. It represents the complementary PMOS and NMOS transistor configuration used to implement the inverter.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/342c8548-025a-4a56-b5a3-6ff0f21207ee" />


## 7. Circuit Simulation Using NGSpice

Pre-layout transient simulation was performed using NGSpice to examine the switching behaviour of the CMOS inverter.

A pulse input is applied to the circuit, and the output response is observed to verify the inverter operation.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/bbedfb69-3849-452e-bebe-1b86bdc826bd" />


## 8. Waveform Analysis

The input and output voltage waveforms are analyzed to verify the logical operation of the inverter.

Expected behaviour:

- When the input is LOW, the output becomes HIGH.
- When the input is HIGH, the output becomes LOW.
- The output follows the logical complement of the input.

![CMOS inverter input and output waveforms](https://github.com/user-attachments/assets/3f0dc52e-a012-4943-918e-9ccda3d42941)

## 9. Physical Layout Using Magic VLSI

The CMOS inverter physical layout was created using Magic VLSI with the SKY130A technology file.

The layout represents the PMOS and NMOS devices and their physical interconnections. The input, output, power, and ground connections are included in the design.

![CMOS inverter physical layout](https://github.com/user-attachments/assets/eba390d5-c272-45eb-8375-c9b469b46d90)

## 10. Design Rule Check (DRC)

Design Rule Checking verifies whether the physical layout satisfies the geometric rules defined by the SKY130A technology.

The DRC check was run in Magic VLSI. The reported output showed:

**Total DRC errors found: 0**

This indicates that no DRC errors were reported in the checked layout.

![CMOS inverter DRC result](https://github.com/user-attachments/assets/7facefdf-7531-45b7-bce3-3211f63550c6)

## 11. Layout Versus Schematic (LVS)

Layout Versus Schematic verification compares the circuit extracted from the physical layout with the original schematic netlist.

The comparison checks transistor types, device connectivity, and circuit topology to determine whether the layout matches the intended schematic.

<img width="1497" height="335" alt="image" src="https://github.com/user-attachments/assets/e75b0f00-50e7-40a3-b4ea-6afe69d0f8c2" />




## 12. Parasitic Extraction and Post-Layout Simulation

Parasitic extraction generates a SPICE representation of the physical layout. Depending on the extraction configuration, the netlist may include parasitic capacitances and resistances.

The extracted netlist can be simulated using NGSpice to evaluate the inverter's switching behaviour and compare the results with the pre-layout simulation.

![CMOS inverter extraction or post-layout simulation](https://github.com/user-attachments/assets/08960bca-5cbb-4f30-b3de-e5002a7810a0)



## 13. Current Project Status

| Project stage | Status |
|---|---|
| EDA environment setup | Completed |
| SKY130A PDK configuration | Completed |
| CMOS inverter schematic design | Completed |
| SPICE testbench and pre-layout simulation | Completed |
| Input/output waveform analysis | Completed |
| Magic VLSI physical layout | Completed |
| Design Rule Check (DRC) | Completed — 0 reported errors |
| Layout Versus Schematic (LVS) |Completed |
| Parasitic extraction | Completed |
| Post-layout simulation | Completed |

## 14. Learning Outcomes

- Understanding the operation of a CMOS inverter.
- Practical experience with schematic design using Xschem.
- Experience with SPICE netlists and NGSpice simulation.
- Analysis of transient input and output waveforms.
- Familiarity with the SKY130A technology environment.
- Experience with physical layout and design rule checking.
- Understanding of LVS verification and parasitic extraction.

## 15. Conclusion

This project demonstrates the CMOS inverter design flow using the SKY130A PDK and open-source EDA tools. The schematic and pre-layout simulation establish the expected circuit behaviour, while the Magic VLSI layout and DRC check extend the project into physical implementation and verification.

LVS and post-layout simulation results will be documented according to the actual verification outputs.

## 16. Author

**G. Pravallika**  
B.Tech – Electronics and Communication Engineering

This is an ongoing learning project documenting CMOS inverter design, simulation, physical layout, and verification using open-source VLSI tools.

## 17. References

- [SkyWater SKY130 PDK](https://github.com/google/skywater-pdk)
- [Open_PDKs](https://github.com/RTimothyEdwards/open_pdks)
- [Xschem](https://github.com/stefanschippers/xschem)
- [Magic VLSI](http://opencircuitdesign.com/magic/)
- [NGSpice](https://ngspice.sourceforge.io/)
- [Netgen LVS](http://opencircuitdesign.com/netgen/)
