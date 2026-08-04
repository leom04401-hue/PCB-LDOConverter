# MIC5317 5V to 3.3V Low-Dropout (LDO) Regulator Breakout Board

A compact, high-performance power regulation module designed in Altium Designer. This board steps down a +5V input supply to a clean, stable +3.3V output rail using the Microchip MIC5317 low-dropout regulator, optimized for low-noise sensor and microcontroller applications.

---

## Key Features & Architecture
* **High-Performance LDO Regulator:** Centered around the MIC5317-3.3, delivering up to 150 mA of continuous output current with a low dropout voltage of 155 mV at full load.
* **Low Noise & High PSRR:** Features a high Power Supply Rejection Ratio (70 dB PSRR), making it ideal for isolating sensitive analog and mixed-signal rails from noisy digital power sources.
* **Ultra-Low Quiescent Current:** Draws only 29 microamps of ground current, ensuring high energy efficiency for battery-powered or portable architectures.
* **Always-Enabled Configuration:** The Enable (EN) pin is tied directly to the input voltage rail (VIN), ensuring immediate power-up upon connection.

---

## Technical Specifications & Component Stack
* **Input Voltage (VIN):** +5V DC (via JST GH 2-pin connector J1)
* **Output Voltage (VOUT):** +3.3V DC (via JST GH 2-pin connector J2)
* **Decoupling Capacitors:** 
  * C1 (1 microfarad, 0805 ceramic) - Input transient bypass
  * C2 (1 microfarad, 0805 ceramic) - Output stability capacitor
* **Design Software:** Altium Designer

---

## Engineering Design Highlights & Best Practices
1. **Capacitor Proximity:** Placed input and output ceramic capacitors (C1 and C2) directly adjacent to the regulator's VIN, VOUT, and GND pins to minimize loop inductance and maintain loop stability.
2. **Clean Ground Return:** Utilized a solid ground reference tied directly to pin 2 (GND) of the regulator, providing a low-impedance return path and effective thermal dissipation.
3. **Connector Integration:** Incorporated robust JST-GH connectors (J1 and J2) with mechanical mounting tabs for secure cable interfacing.

---

## Repository Structure
```text
├── Hardware/
│   ├── Altium_Project/           # .PrjPcb, schematic (.SchDoc), and PCB layout (.PcbDoc)
│   ├── Outputs/                  # Generated Gerber files, NC Drill files, and BOM
├── 3D_Renders/                   # Board preview images (.png)
└── README.md 
```
![PCB Layout](Screenshot%202026-08-04%20164806.png)

