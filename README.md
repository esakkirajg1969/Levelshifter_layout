# LevelShifter Layout

## Project Overview

A **level shifter** is a CMOS circuit used to translate a digital signal
from one voltage domain to another. It enables circuits operating at
different supply voltages to communicate reliably. Level shifters are
commonly used in multi-voltage integrated circuits, where different
blocks may operate using different voltage levels to reduce power
consumption or meet performance requirements.

### Working Principle

This project implements a CMOS level shifter using PMOS and NMOS
transistors. The input signal controls the NMOS pull-down network, while
the cross-coupled PMOS network helps pull the output toward the higher
supply voltage. Depending on the input logic state, the circuit drives
the output to the corresponding logic level in the higher-voltage
domain. This allows a low-voltage-domain signal to be interfaced with a
higher-voltage-domain circuit.

## Project Details

  Parameter               Details
  ----------------------- --------------------------------------------
  Design                  CMOS LevelShifter Layout
  Design Tool             Cadence Virtuoso
  PDK                     gpdk045nm
  Layout Editor           Cadence Virtuoso Layout XL
  Physical Verification   Cadence - Physical Verification System (PVS)
  Verification Checks     DRC, LVS, ERC and PEX

## 1. Schematic Design

The level shifter schematic was created in **Cadence Virtuoso Schematic
Editor** using PMOS and NMOS transistors.

-   Implemented the level shifter circuit using PMOS and NMOS devices.
-   Configured PMOS transistors with a width of **360 nm** and a length
    of **45 nm**.
-   Configured NMOS transistors with a width of **240 nm** and a length
    of **45 nm**.
-   Defined the required input and output pins: **in** and **out**.
-   Added separate supply pins for the two voltage domains: **VDD1** and
    **VDD2**.
-   Added **VSS** as the ground reference.

### Schematic Screenshot

![CMOS Level Shifter Schematic](images/level-shifter-schematic.jpeg)

## 2. Layout Design

The physical layout was implemented using **Cadence Virtuoso Layout XL
Editor**.

-   Placed the PMOS and NMOS devices with a compact arrangement while
    maintaining a symmetrical placement approach.
-   Organized the devices and routing to support the intended level
    shifter connectivity.
-   Used **Metal 1 (M1), Metal 2 (M2) and Metal 3 (M3)** for
    interconnections.
-   Implemented two separate **n-tap** regions for the **VDD1** and
    **VDD2** supply connections.
-   Implemented one **p-tap** region for the **VSS** connection.
-   Completed the layout with the required input, output and supply
    connections.

### Layout Screenshot

![CMOS Level Shifter Layout](images/level-shifter-layout.jpeg)

## 3. Physical Verification

Physical verification was performed using **Cadence Physical
Verification System (PVS)** to check the layout against the design
requirements.

-   **Design Rule Check (DRC):** Completed to check the layout against
    the applicable physical design rules.
-   **Layout Versus Schematic (LVS):** Completed to verify that the
    layout connectivity and devices match the schematic.
-   **Electrical Rule Check (ERC):** Completed to check for electrical
    connectivity and rule-related issues.
-   **Parasitic Extraction (PEX):** Completed to extract parasitic
    components from the physical layout for post-layout analysis.

**Verification Status:** DRC, LVS, ERC and PEX were completed
successfully. The PVS results screenshot shows a clean DRC result and an
LVS comparison match.

### Verification Screenshot

![CMOS Level Shifter Physical Verification
Results](images/level-shifter-verification.jpeg)

## Tools and Technologies

-   **Cadence Virtuoso Schematic Editor** -- Schematic design.
-   **Cadence Virtuoso Layout XL** -- Physical layout implementation.
-   **gpdk045 PDK** -- 45nm generic process design kit.
-   **Cadence PVS** -- Physical verification, including DRC, LVS, ERC
    and PEX.

## Project Outcome

Successfully designed the CMOS level shifter schematic and layout in
Cadence Virtuoso using the gpdk045 PDK. Completed DRC, LVS, ERC and PEX
using Cadence PVS, with the available verification results indicating a
clean DRC run and a matching layout-versus-schematic comparison.
 
 ## Author

**Esakkiraj G**
B.E. Electronics and Communication Engineering
Custom & Analog Layout Engineer

**Domain:** VLSI | Custom Layout | Analog Layout | CMOS Design
