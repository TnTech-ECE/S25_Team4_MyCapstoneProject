# Power Management Subsystem Design

**Prepared by:** Mohammed Almehmadi  
**Subsystem:** Power Management  
**Project:** Modular Greenhouse Monitoring System  
**Department of Electrical and Computer Engineering**  
**Tennessee Technological University**

---

## 1. Function of the Subsystem

The Power Management Subsystem ensures reliable, safe, and efficient electrical delivery to all modules of the greenhouse system — including three ESP32-based sensor units and one Raspberry Pi 4-based central processor.

This design uses:
- 3-cell AA Eneloop Pro battery packs with MT3608 boost converters for ESP32 units.
- A Geekworm X728 UPS HAT with two 20,000mAh USB-C power banks and two 18650 batteries to power the Raspberry Pi.
- The system enables continuous off-grid operation with safe switchover and recharge methods.

---

## 2. Specifications and Constraints

### Specifications (Shall Statements)

1. The subsystem **shall** provide regulated output voltages of 5V or 3.3V depending on module requirements.  
2. Each ESP32 sensor module **shall** be powered by a 3-cell Eneloop Pro AA battery pack with a nominal voltage of 3.6V.  
3. Each ESP32 module **shall** include an MT3608 boost converter to raise the voltage to 5V.  
4. Each sensor module **shall** operate for a minimum of 72 hours per charge cycle( this will be affected by other teammates subsystems).  
5. The Raspberry Pi 4 **shall** be powered by a Geekworm X728 UPS module with dual power bank inputs and internal 18650 batteries.  
6. The UPS **shall** ensure uninterrupted operation of the Raspberry Pi during power bank replacement or failure.

### Constraints (Shall Statements)

1. The subsystem **shall** not exceed 50V DC under any condition, in compliance with OSHA Standard 29 CFR 1910.303.  

2. The 18650 battery cells **shall** operate within 80% depth of discharge to preserve longevity and prevent degradation.  

3. All components **shall** operate safely within a temperature range of 0°C to 60°C.  

4. All electrical materials and connectors **shall** meet ASTM B117 corrosion resistance requirements.  


---

## 3. Overview of Proposed Solution

Each ESP32 module is powered by a 3-cell Eneloop Pro battery pack connected to an MT3608 boost converter. The output is manually tuned to 5V using a multimeter.

The Raspberry Pi 4 is powered by a Geekworm X728 UPS board that:
- Draws primary power from USB Power Bank A
- Switches to USB Power Bank B when needed
- Temporarily bridges power via internal 18650 cells during switching

This allows for uninterrupted Raspberry Pi operation while maintaining modular, user-friendly power management for field deployment.

---

## 4. Interface with Other Subsystems

| Connected Subsystem       | Interface Type     | Direction | Description                                     |
|---------------------------|--------------------|-----------|-------------------------------------------------|
| ESP32 Sensor Boards       | Wired (Vin, GND)   | Output    | 5V from MT3608 boost converter                  |
| Sensors (e.g., Gravity O₂)| Wired (VOUT, GND)  | Output    | 5V regulated                                    |
| Raspberry Pi 4            | USB-C              | Output    | 5V from Geekworm X728 UPS                       |
| USB Power Banks           | USB-A to Micro-USB | Input     | Supplies 5V input to the UPS board              |

---

###5. 3D Model

![3dmodel](3D_Model.png)

###6. Buildable Schematic
![Schematic](Buildable_circuit.png)

###7. Printed Circuit Board Layout
![Schematic](Printed_Circuit_Board_Layot.png)

## 8. Bill of Materials (BOM)

| Ref  | Component                          | Part Number      | Manufacturer    | Distributor         | Qty | Unit Price | Total     | URL                                                                 |
|------|------------------------------------|------------------|-----------------|----------------------|-----|-------------|-----------|----------------------------------------------------------------------|
| U1   | MT3608 Boost Converter             | MT3608           | AITRIP          | Amazon               | 3   | $1.20       | $3.60     | [Link](https://www.amazon.com/dp/B0C858YYQ1)                         |
| B1   | Eneloop Pro AA Battery (10-Pack)   | BK-3HCCA10FA     | Panasonic       | Amazon               | 10  | $45.99      | $45.99    | [Link](https://www.amazon.com/dp/B0D2JBNH4H)                         |
| H1   | 3-AA Battery Holder                | BH3AAW           | Elenco          | Digikey              | 3   | $1.50       | $4.50     | [Link](https://www.digikey.com)                                     |
| D1   | LED (3mm Red)                      | LTL-307EE        | Lite-On         | Digikey              | 3   | $0.50       | $1.50     | [Link](https://www.digikey.com)                                     |
| R1   | Resistor 330Ω                      | CF14JT330R       | Stackpole       | Mouser               | 3   | $0.05       | $0.15     | [Link](https://www.mouser.com)                                      |
| P1   | JST Connector Pair                 | B2B-PH-K-S       | JST             | Digikey              | 12  | $0.30       | $3.60     | [Link](https://www.digikey.com)                                     |
| PWR  | USB-C Power Bank (20,000mAh)       | B07SQ5MQ6K       | Anker           | Amazon               | 2   | $54.99      | $109.98   | [Link](https://www.amazon.com/dp/B07SQ5MQ6K)                         |
| UPS  | Geekworm UPS Board for Raspberry Pi| X728             | Geekworm        | Geekworm             | 1   | $43.00      | $43.00    | [Link](https://geekworm.com/products/x728)                          |
| B2   | 18650 Li-ion Battery (Flat-Top)    | INR18650-25R     | Samsung         | 18650BatteryStore    | 2   | $3.99       | $7.98     | [Link](https://www.18650batterystore.com/products/samsung-25r-18650)|
| CBL  | USB-A to Micro-B Cable             | DH-20M50057      | Cvilux USA      | Digikey              | 2   | $1.15       | $2.30     | [Link](https://www.digikey.com/en/products/detail/cvilux-usa/DH-20M50057/13177527) |

**Total BOM Cost: $221.20**
---

## 9. Analysis

- This power management design ensures continuous, modular, and off-grid-capable operation of all critical subsystems.
- It utilizes reliable Eneloop Pro AA batteries for sensor modules and a dual power bank + UPS strategy for the Raspberry Pi 4.
- The integrated kill switch provides an essential function:
  - It allows the user to safely disconnect power during power bank replacement without disrupting Raspberry Pi operation.
  - When a power bank runs low, the user activates the kill switch, swaps in a fully charged power bank, and re-engages power — all without requiring reboot or rewiring.
  - This process minimizes the risk of data corruption and ensures system uptime.
- Although this architecture is more expensive than traditional SLA-battery or relay-based systems, it offers major benefits:
  - **Usability**: Power banks are easy to swap and recharge.
  - **Modularity**: Each component is independently serviceable.
  - **Field efficiency**: No special tools or skills are needed.
- The use of swappable USB-C power banks allows users to recharge devices with common, readily available charging equipment.
- The Geekworm X728 UPS handles automatic switchovers between sources, eliminating the need for manual switches or relays and reducing user error.
- This investment in a smarter, user-friendly design saves **time, energy, and maintenance costs** over the long term.
- It is especially advantageous in remote or high-humidity environments like greenhouses, where uninterrupted operation and easy maintenance are critical.

 ---

## 10. References

[1] Occupational Safety and Health Administration (OSHA), "Standard 29 CFR 1910.303 – General Requirements," OSHA Regulations, [Online]. Available: https://www.osha.gov/laws-regs/regulations/standardnumber/1910/1910.303

[2] Amazon, "MT3608 Boost Converter Module," Amazon.com, [Online]. Available: https://www.amazon.com/dp/B0C858YYQ1

[3] Espressif Systems, ESP-WROOM-32 Datasheet, 2020. [Online]. Available: https://www.espressif.com/sites/default/files/documentation/esp-wroom-32

[4] Olimex Ltd., MT3608 Step-Up Converter Module Datasheet. [Online]. Available: https://www.olimex.com/Products/Breadboarding/BB-PWR-3608/resources/MT3608.pdf

[5] ChatGPT. (2025). AI-based text refinement for improved structure, readability, and formatting. OpenAI.

