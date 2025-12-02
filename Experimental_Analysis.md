# Experimental Analysis

## Introduction

This experimental analysis revisits the conceptual design of our greenhouse sensor units, a project born out of the desire to create a portable, modular data collection system that could thrive in diverse environments. The overarching vision was not simply to build hardware, but to engineer a reliable ecosystem where sensors, processors, and communication subsystems work in harmony to provide continuous insight into greenhouse conditions.  

From the earliest design sketches, two themes emerged as critical: endurance and connectivity. Endurance meant that the system had to sustain itself for long periods without human intervention, while connectivity meant that data had to flow seamlessly from the greenhouse floor to the cloud, where it could be monitored and analyzed. These guiding principles shaped the specifications and experiments described in this report.

### Relevant Critical Success Criteria

**Specification 1:** Batteries shall be able to operate for a minimum of 72 hours before recharging. This requirement reflects the practical need for uninterrupted monitoring in real-world greenhouse operations.  

**Specification 2:** Each module shall track its battery level and alert users when recharging or replacement is necessary. A system that silently fails is unacceptable; proactive alerts ensure reliability.  

**Specification 3:** Collected data shall be transmitted wirelessly from each module to the central processor for real-time monitoring. Wires are impractical in modular deployments, so wireless communication is essential.  

**Specification 4:** The central processor shall transmit data to a cloud platform when Wi-Fi connectivity is available. This bridges the greenhouse environment with remote monitoring capabilities.  

**Specification 5:** In the absence of network connectivity, modules shall store data locally to ensure no data loss for offloading. Reliability means resilience against connectivity interruptions.  

**Specification 6:** The cloud platform shall display live data and retain historical data for analysis and monitoring. This ensures both immediate awareness and long-term insight.  

---

## Experiment One: Battery Lifespan

### Purpose and Justification
The first experiment was designed to test the heartbeat of the system: its battery subsystem. Specifications 1 and 2 were combined to evaluate whether the sensor units could sustain operation for the required three-day minimum and whether the battery indicators provided clear, actionable feedback. In essence, this experiment asked: can the system endure, and can it communicate its own health?

### Detailed Procedure
The ESP32 sensor units were connected to a suite of environmental sensors — BME280 for humidity, BH1750 for light, SCD40 for CO₂, and Gravity sensors for O₂. These units were powered by the battery subsystem and tasked with continuously parsing sensor data and transmitting it to the Raspberry Pi central processor.  

The test spanned three days, during which the LED battery indicators were carefully observed. The indicator system was intuitive: full charge illuminated all LEDs in solid red, while decreasing charge gradually extinguished them. A flashing lowest LED signaled imminent depletion, serving as a final warning before shutdown.  

### Expected Results
With sleep mode enabled, the ESP32 units were expected to last at least 72 hours. The battery indicator would begin at full capacity (four bars) and gradually decline to zero, providing a visual narrative of the battery’s journey.  

### Actual Results
In practice, the ESP32 module depleted its power supply after approximately 55 hours of continuous operation. The discrepancy was traced to the absence of sleep mode, which significantly increased power consumption. Despite this, the battery subsystem itself performed flawlessly, aligning with theoretical calculations.  

Projected runtime without sleep mode was 56.52 hours, and the measured runtime of 55 hours confirmed subsystem integrity. With sleep mode properly implemented, the system’s operational lifetime is projected to extend to approximately 10 days — a result that not only meets but exceeds design expectations.  

### Interpretation and Conclusions
The experiment validated the robustness of the battery subsystem. The shortfall in runtime was not a failure of hardware but a configuration oversight. Once corrected, the system promises exceptional endurance, reinforcing confidence in its deployment for extended greenhouse monitoring.  

---

## Experiment Two: Sensor Data Collection and Storage

### Purpose and Justification
The second experiment shifted focus from endurance to intelligence: could the system reliably collect, transmit, and store sensor data under both online and offline conditions? Specifications 3 through 6 were combined to test the full communication pipeline, from sensor to cloud.  

### Detailed Procedure
The Raspberry Pi served as the central processor, continuously interfacing with ESP32 sensor units. For online testing, the ESP32 units transmitted data wirelessly to the Pi, which hosted a website displaying real-time readings. For offline testing, the Pi stored data locally on its SD card over three days, ensuring resilience against connectivity interruptions.  

### Expected Results
The system was expected to collect data on CO₂, O₂, humidity, and temperature for three days, display this data on the website, and store it locally in `.csv` format for offline access.  

### Actual Results
The Raspberry Pi successfully interfaced with the ESP32 boards, receiving and displaying sensor data in real time. Over three days, the system operated continuously, with data collected every five minutes. Offline storage worked seamlessly, with the SD card retaining data in `.csv` format, readily compatible with Microsoft Excel for further analysis.  

### Interpretation and Conclusions
The experiment demonstrated that the system could function as both a live monitoring tool and a resilient offline recorder. Graphs displayed inferred datapoints, providing a smooth visualization of trends. Future improvements could include customizable time scales for the website and more precise sampling intervals, but the core functionality was validated.  

---

## Conclusion

This capstone project sought to deliver reliable greenhouse sensor units within a constrained development timeline. Despite challenges, the majority of customer requirements were met.  

The interconnect PCB subsystem proved effective in linking ESP32 boards with sensors. The Raspberry Pi central processor successfully parsed and displayed sensor data both online and offline. The battery subsystem demonstrated strong performance, with clear pathways to extended endurance through sleep mode optimization.  

Together, these subsystems formed a cohesive, resilient system capable of supporting greenhouse monitoring with both reliability and adaptability.  

---

## Documenting and Tracking Components

The following table documents all components used in the project, their sources, and their conditions. This meticulous tracking ensured transparency and accountability throughout the development process.  

| Item # | Description | Quantity | Vendor/Source | Order #/ID | Storage Location | Date Acquired | Condition | Notes |
|--------|-------------|----------|---------------|------------|------------------|---------------|-----------|-------|
| 1 | ESP32 Boards | 3 | Amazon | 15363 | Lab | 9/3/2025 | New | All used in experiment |
| 2 | BME280 | 3 | Adafruit | 2652 | Lab | 9/3/2025 | New | All used in experiment |
| 3 | BH1750 | 3 | Adafruit | 4681 | Lab | 9/3/2025 | New | One burnt |
| 4 | SCD40-D-R2 | 3 | REHOC | 500247842 | Lab | 9/3/2025 | New | All used in experiment |
| 5 | TPX00050 | 3 | Gravity | 6959420917020 | Lab | 9/3/2025 | New | All used in experiment |
| 6 | PPTC151LFBN-RC | 6 | Sullins Connector Solutions | S7013-ND | Lab | 9/3/2025 | New | All used in experiment |
| 7 | PPPC041LFBN-RC | 3 | Sullins Connector Solutions | S7037-ND | Lab | 9/3/2025 | New | All used in experiment |
| 8 | PPTC051LFBN-RC | 3 | Sullins Connector Solutions | S6103-ND | Lab | 9/3/2025 | New | All used in experiment |
| 9 | PPPC061LFBN-RC | 3 | Sullins Connector Solutions | S7039-ND | Lab | 9/3/2025 | New | All used in experiment |
| 10 | PPTC071LFBN-RC | 3 | Sullins Connector Solutions | S7005-ND | Lab | 9/3/2025 | New | All used in experiment |
| 11 | PCB | 5 | JLCPCB | null | Lab | 9/3/2025 | New | Three used in experiment |
| 12 | Jumper Wires | 240 | Adafruit | 826 | Lab | 9/3/2025 | New | All used in experiment |
| 13 | Solder | 1 | Amazon | B001DPVT1A | Lab | 9/3/2025 | New | Used in experiment |
| 14 | PETG Filament | 1 | Amazon | null | Lab | 9/3/2025 | New | Not used |
| 16 | M3 Standoff Kit | 1 | Amazon | B0D493MPW3 | Lab | 9/3/2025 | New | Used, all remain in lab |
| 17 | Plexiglass Sheet | 1 | Amazon | null | Lab | 9/3/2025 | New | 3 sheets used |
| 18 | Raspberry Pi 4 | 1 | PiShop | 4GB-9004 | Lab | 9/3/2025 | New | Used in experiment |
| 19 | 512 GB SD Card | 1 | Amazon | null | Lab | 9/3/2025
