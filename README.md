# Microelectronics: Custom Mini-PDK for Microwind

This repository contains a Custom Mini-PDK (Process Design Kit) and a set of CMOS layouts developed in Microwind. The project focuses on practical VLSI design, bridging the gap between theoretical circuit concepts and physical layout implementation.

## Technical Foundation

The design rules and layout constraints implemented in this PDK are strictly guided by the industry-standard textbook:
> **"CMOS VLSI Design: A Circuits and Systems Perspective"** by Neil Weste and David Harris.

The project utilizes **lambda-based ($\lambda$) scalable design rules** to ensure that the layouts can be adapted across different sub-micron technology nodes.

---

## Development Philosophy

The project follows a tiered development strategy:

1.  **Functional Verification:** The primary goal is ensuring the logical and electrical correctness of the cells.
2.  **Area Optimization:** Layouts are crafted with a focus on high-density and minimal footprint, pushing for the most compact cells possible within the design rules.
3.  **Future Characterization:** Once functionality and area are stabilized, the next phase will involve a rigorous analysis of:
    * Parasitic Capacitances (Poly, Diffusion, and Overlap).
    * Propagation Delays ($t_{pd}$).
    * Static and Dynamic Power Consumption.

---

## Project Structure

| Component | Description | Status |
| :--- | :--- | :--- |
| pdk-rules/ | Configuration files and design rule documentation. | In Progress |
| cells/ | Standard cells (Inverters, NAND, NOR, Pass Gates). | Functional |

---

## Design Rules Synthesis

Below is a synthesis of the design rules applied to this PDK (Polysilicon, Diffusion, and Metal layers) according to the Weste and Harris guidelines:



![Design Rules Synthesis](pdk-rules/rules_synthesis.png)

---

## How to Use

1. **Clone** this repository to your local machine.
2. Open **Microwind**.
3. Go to **File** -> **Select Foundry** and load the rule file found in the `/pdk-rules` folder.
4. Open any **.MSK** file from the `/cells` folder to visualize and simulate the layout.

---

## License
This project is for educational and practice purposes.
