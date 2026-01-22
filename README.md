# LTC3807_Buck_Converter_LTspice
Datasheet-based design and LTspice simulation of a 5 V to 1 V synchronous buck converter using the LTC3807 controller

# LTC3807 Buck Converter – LTspice Simulation

This project demonstrates the design and simulation of a synchronous buck converter
based on the **LTC3807** controller, implemented and verified in **LTspice**.

The goal is to meet strict output voltage and ripple requirements using
component selection guided by the LTC3807 datasheet.

---

## 🔧 Project Specifications

- **Input Voltage (VIN):** 5 V
- **Output Voltage (VOUT):** 1.0 V ± 30 mV (DC + ripple)
- **Load Current Range:** 10 mA – 2 A
- **Topology:** Synchronous buck converter
- **Controller IC:** LTC3807
- **Simulation Tool:** LTspice

---

## ⚙️ Design Approach

The design follows the recommended procedure in the LTC3807 datasheet:

### Output Voltage Setting
- Feedback network calculated using the internal 0.8 V reference
- Resistor values selected for VOUT ≈ 1.0 V

### Switching Frequency
- Switching frequency set to approximately **300 kHz**
- Selected as a compromise between efficiency, ripple, and component size

### Inductor Selection
- Inductor value chosen to achieve ~30% peak-to-peak ripple current at full load
- Nominal inductance: **4.7 µH**
- Inductor current rating selected with margin above 2 A

### Current Sense Resistor
- Sense resistor selected to allow current limiting slightly above 2 A
- Rsense ≈ **0.025 Ω**

### Output Capacitor Selection
- Output ripple budget split between ESR ripple and capacitive ripple
- Low-ESR ceramic capacitors used
- Total effective output capacitance selected to ensure ripple < 30 mV

---

## 📊 Simulation Results

The LTspice simulation verifies:
- Stable regulation at 1.0 V output
- Output voltage ripple within specification
- Proper operation across the full load current range
- Acceptable inductor current ripple and current limit behavior

Screenshots and waveform plots are included in the repository.

---

## 📁 Repository Contents

- LTspice schematic (.asc)
- Simulation plots
- Component calculations
- Project description and design rationale

---

## 🧠 Purpose of the Project

This project is intended to demonstrate:
- Datasheet-driven power electronics design
- Practical component selection
- Understanding of buck converter operation
- Ability to verify performance through simulation

---

## 🛠 Tools Used

- LTspice
- LTC3807 datasheet (Analog Devices)
