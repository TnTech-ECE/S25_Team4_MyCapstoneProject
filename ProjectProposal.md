# Portable Sensory Network

## Introduction 

As technology continues to advance, its integration into agriculture is becoming increasingly vital [9]. Greenhouses provide controlled environments for plant growth, but managing these conditions effectively requires continuous monitoring of factors such as temperature, humidity, CO₂ levels, light intensity, and oxygen concentration. This project aims to design a portable sensory network for greenhouses to improve climate consistency and enhance experimental accuracy.

This system will serve two main purposes:

1. **Improving Climate Consistency:** Greenhouses often experience uneven temperature and climate conditions across different areas. This inconsistency can stress plants, reduce growth rates, and make it difficult to maintain ideal conditions. The sensory network will enable precise monitoring of temperature, humidity, and CO₂ levels throughout the greenhouse, allowing for targeted adjustments and more uniform conditions.

2. **Enhancing Experimental Accuracy:** When conducting research and experiments to understand plant behaviors, it's essential to have a clear and accurate picture of the environmental conditions throughout the plant canopy. By integrating sensors that monitor light intensity, temperature, and humidity at multiple levels and locations, the system will provide the necessary data to ensure consistent and reproducible experimental conditions.

By combining real-time environmental monitoring with camera-based plant growth tracking, this system will not only optimize growing conditions for educational purposes but also contribute to advanced research into plant growth behaviors.

## Formulating the Problem

A major challenge in greenhouse monitoring is the inconsistent distribution of temperature and humidity readings due to fixed sensor locations [8]. This can lead to uneven plant growth and unreliable data for research. The group’s aim is to work with Dr. Kinmonth-Schultz, as well as the Biology Department at Tennessee Tech, to make a sensory network that will collect data on the specific variables mentioned above. Website design, data storage, hardware implementation, and running wires require a diverse set of engineers and minds to engineer a solution to these problems. All solutions that are currently available have soaring prices, and other specific devices might be required. There seems to be no all-in-one solution for this application.

### Background

Effective greenhouse management relies on precise control of environmental factors such as temperature, humidity, CO₂ levels, oxygen concentration, and light intensity. However, maintaining uniform conditions throughout a greenhouse is challenging due to spatial variations caused by airflow patterns, structural differences, and equipment placement. These inconsistencies can negatively impact plant growth, resource efficiency, and the accuracy of scientific research conducted in greenhouse settings.

A key limitation of current monitoring solutions is their reliance on fixed sensor placements, which fail to account for localized microclimates. Without flexible and portable sensing capabilities, greenhouse operators and researchers may be unable to detect subtle environmental variations that influence plant health and growth patterns. Moreover, commercially available sensor networks are often expensive, proprietary, and difficult to customize, making them impractical for smaller research facilities or educational institutions [5].

The Biology Department at Tennessee Tech, which specializes in botany and plant sciences, has identified these limitations as a barrier to conducting precise research and optimizing greenhouse environments. Existing solutions do not provide sufficient mobility, scalability, or cost-effectiveness to meet their needs.

This project addresses these challenges by developing a portable, wireless sensory network designed for flexible deployment within greenhouses. By capturing high-resolution environmental data across multiple locations, this system will provide a more accurate representation of greenhouse conditions while remaining adaptable to different research and agricultural applications.


## Specifications

The system will meet the following requirements to ensure portability, reliability, and usability:

1. **Portability & Size**
   - Modules shall be lightweight and compact for easy deployment and relocation.
   - Modules shall be designed to minimize physical footprint while maintaining functionality.

2. **Power & Energy Management**
   - Modules shall operate on battery power to eliminate the need for permanent wiring.
   - Batteries shall support a minimum operational time of 72 hours before requiring a recharge.
   - Power levels shall be monitored and reported to ensure timely recharging or replacement.

3. **Data Collection & Transmission**
   - Sensors shall measure CO₂, O₂, light intensity, temperature, and humidity at configurable intervals.
   - Modules shall transmit data wirelessly to a central processor via WiFi (when available).
   - If the internet is unavailable, modules shall store data locally for later retrieval.

4. **User Interface & Data Management**
   - A web-based dashboard shall provide real-time monitoring and historical data visualization.
   - Users shall be able to access average values across sensors and view individual sensor data on demand.
   - The system shall allow data to be manually offloaded via USB or SD card when needed.

5. **Environmental Considerations**
   - Modules shall withstand greenhouse conditions, including humidity, dust, and temperature fluctuations.
   - The enclosure shall provide sufficient protection to prevent sensor degradation.
## Constraints

The system will be designed to operate efficiently within the greenhouse environment while adhering to safety and regulatory requirements:
### Environmental Conditions
1. The device shall function in a high-humidity, dust-prone, and water-exposed environment without failure.
2. The device shall meet the IP67 standard for environmental protection, as it provides cost-effective and efficient protection in greenhouse environments.
3. Enclosures and components shall be resistant to moisture and particulate matter to ensure longevity and reliability.
4. The enclosures and components shall meet an Ingress Protection (IP) rating of:
   - IP65 or higher for protection against dust and low-pressure water jets.
   - IP67 if additional submersion resistance is required.
   - The enclosures shall comply with NEMA 4X as an alternative to IP ratings, providing dust-tight, watertight, and corrosion-resistant enclosures.
6. The materials used in enclosures and components shall comply with ASTM B117 for salt fog resistance in corrosion-prone areas.

### Power Limitations

7. The system shall not exceed 50V operating voltage to comply with OSHA regulations.
8. The power supply and electrical components shall be designed for safe operation in greenhouse conditions to prevent electrical hazards.
9. The system shall comply with the following OSHA Regulations for electrical safety:
   - 29 CFR 1910.303 for general electrical safety compliance.
   - 29 CFR 1910.307 for electrical safety in wet/damp locations.
   - 50V or lower DC systems classified as "low voltage" per OSHA standards.

### Safety & Regulatory Compliance

10. The actuation circuits shall include overload protection to prevent damage or fire risks.
11. The system shall comply with the National Electrical Code (NEC) regulations for greenhouse installations, including:
   - NEC Article 547, which covers electrical safety requirements for agricultural buildings, including greenhouses.
   - NEC 210.8(B), which mandates GFCI protection for 15A & 20A, 120V outlets in damp/wet locations.
   - NEC 250.32, which specifies grounding requirements for separate structures.
12. The system shall comply with the following circuit protection standards:
   - UL 943 for GFCI safety compliance.
   - UL 1449 for surge protection device compliance.

### Sensor & Actuator Integration

13. The sensor network shall properly interface with actuators to ensure accurate responses based on environmental data.
14. The sensors and actuators shall be designed to function consistently despite greenhouse conditions, including high humidity, dust, and temperature variations.

## Survey of Existing Solutions

Existing solutions for greenhouse monitoring range from DIY approaches to industrial-grade systems:

- **DIY Solutions:** Numerous YouTube videos showcase small-scale "backyard greenhouse" monitoring systems. While these are cost-effective, they often lack accuracy, durability, and advanced data management features needed for reliable operation in larger setups [5].
- **Industrial Solutions:** Several companies offer high-end sensors and software for commercial greenhouse management. However, these solutions are often cost-prohibitive for small to mid-sized projects, making them impractical for this application.

Below are multiple current solutions, complete with lists of reasons as to why any particular solution would not work for solving this problem.

*iGrow 800 Environmental Controller [12]: Provides advanced environmental monitoring, including temperature, humidity, and CO₂ control, but comes at a high cost of $4,145.00.

   - Cons: 
     - Expensive and may be overkill for smaller greenhouse operations.
     - Does not include oxygen monitoring.

*WIFI Greenhouse Monitoring System from ACF Greenhouses [13]: Priced at $69.00, this system offers affordable monitoring but does not address issues related to varying temperature gradients in a greenhouse.

   - Cons: 
     - Limited functionality and lacks advanced environmental control features.
     - Does not include oxygen monitoring or light intensity sensors.
     - No offline portability.

*Sensaphone 1800 [14]: Allows monitoring of up to 8 locations within a greenhouse enclosure at a cost of $1,014.95, providing remote alerts for environmental changes.

   - Cons: 
     - High upfront cost.
     - Primarily focuses on monitoring rather than automated control.
     - Lacks modularity and portability due to requiring telephone lines. 

*ECLIPSE F90 Master Environmental Controller [16]: This controller offers precise monitoring and control of temperature, humidity, and CO₂ levels from a centralized unit. It features three digital screens displaying real-time data, along with LED indicators for active modes and errors.

   - Cons: 
     - Complex setup and may require additional sensors for full functionality.
     - Does not include oxygen monitoring or light intensity sensors.
     - No offline portability and offloading of data. 

*Monnit Wireless Sensor Systems [17]: A comprehensive solution that includes wireless sensors to monitor temperature, humidity, light levels, soil moisture, and HVAC performance. Pricing varies depending on sensor configurations.

   - Cons: 
     - It can become expensive when multiple sensors are needed. 
     - Wireless connectivity may be unreliable in certain greenhouse environments.
     - Does not include oxygen monitoring or light intensity sensors.
     - No offline portability and offloading of data.

*Ceres SunSense™ Controller [18]: A centralized system designed for advanced greenhouse control, tracking parameters such as temperature, relative humidity, CO₂ levels, leaf/canopy temperature, and PAR (photosynthetically active radiation). Custom pricing available based on configuration.

   - Cons: 
     - High cost and complexity.
     - Requiring a learning curve for proper setup and management.
     - Does not include oxygen monitoring or light intensity sensors.
     - No offline portability and offloading of data.

*EDYCARX CO₂ Controller [19]: A digital controller that monitors and regulates CO₂ levels, temperature, and humidity, commonly used in grow rooms and greenhouses. Available for purchase on Amazon, with pricing typically around $300.

   - Cons: 
     - Primarily focused on CO₂ monitoring.
     - Lacks broader environmental controls such as light intensity and oxygen concentration.
     - Does not include oxygen monitoring or light intensity sensors.
     - No offline portability and offloading of data.

*INKBIRD CO₂ Controllers [20]: Designed for grow tents, greenhouses, and ventilation systems, these controllers help maintain optimal CO₂ levels, improving plant growth efficiency. Prices range from $100 to $400 depending on features.

   - Cons: 
     - Limited to CO₂ regulation, requiring additional systems for full greenhouse management.
     - Does not include oxygen monitoring or light intensity sensors.
     - No offline portability and offloading of data.

*Sensaphone 400 Monitoring System: A smaller-scale alternative to the Sensaphone 1800, capable of monitoring up to four environmental conditions, including temperature, humidity, and power failures. Priced around $455.00, making it a more affordable option for smaller greenhouses.

   - Cons: 
     - Limited input capacity (only 4 monitoring points), making it unsuitable for larger greenhouses with more complex monitoring needs.
     - Does not include oxygen monitoring or light intensity sensors.
     - No offline portability and offloading of data.

Despite the availability of these solutions, challenges such as cost, scalability, integration, and customization remain key factors in selecting the ideal greenhouse monitoring system. The development of a new solution should address these limitations by offering affordability, modularity, ease of use, and enhanced integration with existing greenhouse infrastructure.

This project aims to bridge the gap between these two extremes by developing a cost-effective, accurate, and scalable greenhouse monitoring system.

## Measures of Success

The success of this project will be evaluated based on its ability to meet functional, technical, and usability requirements in a greenhouse environment. The following key performance indicators (KPIs) and verification methodologies will be used to ensure the system meets its specifications and constraints.

### 1. Sensor Accuracy and Reliability  
**Objective:** Ensure that the system provides precise and reliable environmental readings.  
**Methodology:**  
- **Calibration Testing:** Compare sensor readings against existing-use calibration devices for CO₂, humidity, light intensity, temperature, and oxygen concentration.  
- **Environmental Stress Testing:** Expose sensors to various humidity and temperature conditions to verify their stability and accuracy over extended periods.  
- **Data Consistency Checks:** Deploy multiple sensors in the same location and compare their readings to detect discrepancies or sensor drift.

### 2. Data Acquisition and Transmission  
**Objective:** Ensure efficient data collection, storage, and wireless transmission.  
**Methodology:**  
- **Real-Time Data Logging:** Verify that the system continuously records environmental data without interruptions.  
- **Wireless Communication Range Test:** Measure the effective range of the WiFi or MQTT-based data transmission by placing sensors at increasing distances from the central processing unit (Raspberry Pi).  
- **Offline Data Storage Verification:** Disable the internet connection and ensure data is stored locally and successfully retrieved later.  
- **Data Latency Evaluation:** Measure the time delay between sensor readings and data display on the web interface to ensure near real-time monitoring.

### 3. Power Efficiency and Battery Life  
**Objective:** Verify that the system meets power constraints and maintains long operational times.  
**Methodology:**  
- **Battery Discharge Testing:** Fully charge the system’s batteries and track how long it operates under normal usage conditions.  
- **Power Consumption Profiling:** Measure energy usage of each module and identify any excessive power draws.  
- **Sleep Mode Effectiveness:** Evaluate how implementing low-power modes affects system longevity without compromising data collection.  

### 4. System Durability and Environmental Resilience  
**Objective:** Ensure the system withstands greenhouse conditions, including high humidity, temperature fluctuations, and dust.  
**Methodology:**  
- **Moisture and Dust Resistance Testing:** Place modules in high-humidity conditions and verify functionality over an extended period.  
- **Temperature Endurance Test:** Expose sensors to expected greenhouse temperature extremes and assess performance degradation over time.  
- **Physical Durability Assessment:** Simulate accidental drops or rough handling to confirm robustness of enclosures and wiring.

### 5. Usability and User Experience  
**Objective:** Ensure ease of installation, operation, and data interpretation.  
**Methodology:**  
- **User Testing with Researchers and Greenhouse Staff:** Gather feedback from intended users on system setup, usability, and data accessibility.  
- **Dashboard Functionality Testing:** Verify that the web interface correctly displays real-time and historical data, with intuitive controls.  
- **Error Handling and Troubleshooting:** Simulate sensor failures and network interruptions to evaluate how the system detects issues and notifies users.

### 6. Cost-Effectiveness and Scalability  
**Objective:** Ensure that the system provides an affordable alternative to commercial solutions and can be expanded for future use.  
**Methodology:**  
- **Cost Analysis:** Compare total project cost with commercial greenhouse monitoring systems.  
- **Modular Expansion Test:** Add additional sensors to verify that the system can handle increased data loads without performance degradation.  
- **Long-Term Maintenance Assessment:** Document required maintenance efforts and component replacement frequency to evaluate system longevity.

By meeting these success criteria, the project will demonstrate its effectiveness in bridging the gap between low-cost DIY solutions and expensive industrial-grade greenhouse monitoring systems.

## Resources

This project will require a combination of hardware components, power sources, and communication protocols to ensure reliable data collection and system operation. Key resources include:

#### Hardware Components
1. Environmental Sensors: 
   - CO₂ sensors
   - Humidity sensor
   - Sunlight intensity sensor
   - Temperature sensor
2. Processing Unit: A central processing unit (CPU) to aggregate and manage sensor data.
3. Power Supply: The system will be powered via battery to ensure portability and continuous operation.

#### Data Storage & Transmission

- Wireless Communication: Sensors will transmit data wirelessly to the processing unit for real-time monitoring.
- Onboard Storage: When network transmission is unavailable, data will be stored locally for later retrieval.
- Data Offloading: Stored data should be retrievable via USB drive to be uploaded to the system’s web interface when needed.

#### Network & Communication Protocol
- The MQTT protocol will be used for sensor communication, allowing efficient data transfer over a low-bandwidth network through the ESP32 microcontrollers.
- The collected data will be uploaded to a live webpage, enabling users to monitor and manually control modules remotely.

This resource plan ensures the project is equipped with the necessary components for efficient, real-time environmental monitoring in a greenhouse setting.

### Budget
The estimated budget for the project is outlined below:

| Item | Description | Quantity | Cost |
|------|-------------|----------|------|
| Raspberry Pi | Central Microcontroller | 1 | $35 |
| ESP-WROOM-32 | Sensors Microcontroller | 4 | $12 per 4|
| Eneloop Pro | Batteries | 10 | $36.45 per 8 |
| BME280 | Humidity Sensor | 1 | $15.99 per 2 |
| BH1750 | Light Measurement | 1 | $7.49 per 3 |
| MG811 | CO₂ Monitoring | 1 | $49.90 |
| MT3608 | Boost Converter | 1 | $5.99 per 5 |
| AlphaSense O2-A3 Oxygen Sensor | Oxygen Sensor | 1 | $82 |
| 3D Printing Plastic Filaments | Used for Case Prototype | 1 | $12.99 |
| DS18B20 | Temperature Sensor | 1 | $9.95 |

- Primary Costs: The largest expenses will be for sensors and batteries to power the system [6].
- Sensor Pricing: Individual sensor costs range between $7 - $20 each, depending on type and functionality [2][3][4][7][15][22].
- Processing Unit: A Raspberry Pi 4 ($35) will serve as the central microcontroller [1].
- A sloped plastic chassis will be designed to house the components such that the sensors are protected from the environment costing us the price of the filament ($12.99). 
- Estimated Total: Given the number of sensors and power components needed, the project budget is estimated to cap at $1000.

### Personnel

The project team possesses a strong foundation in Electrical Engineering, ensuring the ability to learn and apply necessary technical skills for successful completion.

- Educational Background: Each team member has completed the prerequisite Electrical Engineering courses, providing a solid foundation in circuit design, embedded systems, and power systems.
- Practical Experience: Some team members have completed internships, gaining hands-on experience in team collaboration, problem-solving, and project development.
- Skill Development: The team is prepared to learn new materials as needed, ensuring the project is executed efficiently and meets all design requirements.
- Infrastructure Impact: The addition of wiring and sensors within the greenhouse may lead to unexpected interactions with the environment, such as interference with plant growth, maintenance challenges, or potential disruptions in greenhouse operations.
- Long-Term Cost Considerations: While the system may increase initial power usage, optimizing energy efficiency and automating data collection could lead to long-term savings by improving resource management and reducing manual labor.

Duy Tran: LTSpice, KiCAD, Power Electronic Topologies, C/C++, Microcontrollers, MATLAB

Henry Hurst: Inventor, LTSpice, Digital System Design, C/C++/R/MATLAB

Michael Feiel: LTSpice, C/C++/Python, Interfacing, Microcontrollers

Mohammed Almehmadi: LTSpice, Power Electronics


These broader implications highlight the importance of balancing power efficiency, system integration, and long-term sustainability for effective greenhouse monitoring.
 
### Timeline

<img src="resources/gantt-chart.png" alt="Gantt Chart" width="auto" height="400"> 

## Specific Implications

The implementation of the greenhouse sensor network will have the following key implications:

- Accurate Data Acquisition: The system will provide precise, real-time measurements of environmental conditions, ensuring optimal monitoring of plant growth factors.
- Visual Growth Monitoring: A visual feed will allow users to track plant development over time, enabling better analysis and decision-making.
- User-Friendly Data Access: The system will present data in an easy-to-understand format, ensuring that general users can interpret and utilize the information effectively.
- Functionality of Sensors: The ideal CO2 Sensor creates heat, which in turn would interfere with the temperature measurements. However, this can be avoided by placing the CO2 above the other sensors.

By integrating these features, the project will improve greenhouse management efficiency and support data-driven decision-making for plant growth optimization.

## Broader Implications

The implementation of the greenhouse sensor network will have several economic and operational impacts:
Pros
- Food Security and Supply Chain Efficiency: Increased efficiency in greenhouse operations could lead to higher crop yields and more reliable production cycles. This has implications for local food security, reducing dependency on imports and strengthening regional food systems. 
- Technology Advancement and Knowledge Sharing: The adoption of advanced monitoring systems could drive innovation in agricultural technology, potentially leading to knowledge-sharing initiatives or influencing policy decisions regarding sustainable farming practices. 
- Economic Growth and Workforce Evolution: While automation reduces manual labor in certain areas, it also creates new opportunities in agricultural technology, data analytics, and system maintenance, fostering a shift in the skills required for future agricultural workforces.
Pros/Cons
- Energy Consumption: While the system requires power to operate, implementing sleep modes on certain sensors and cameras will help reduce overall power consumption, making the system more energy efficient.
- Infrastructure Impact: The addition of wiring and sensors within the greenhouse may lead to unexpected interactions with the environment, such as interference with plant growth, maintenance challenges, or potential disruptions in greenhouse operations.
- Long-Term Cost Considerations: While the system may increase initial power usage, optimizing energy efficiency and automating data collection could lead to long-term savings by improving resource management and reducing manual labor.

These broader implications highlight the importance of balancing power efficiency, system integration, and long-term sustainability for effective greenhouse monitoring.

## References

[1] DATASHEET raspberry pi 4 model B. (n.d.). https://datasheets.raspberrypi.com/rpi4/raspberry-pi-4-datasheet.pdf 

[2] Adafruit. (n.d.-a). https://cdn-learn.adafruit.com/assets/assets/000/115/588/original/bst-bme280-ds002.pdf?1664822559= 

[3] Digital 16bit serial output type ambient light sensor IC. (n.d.-c). https://www.mouser.com/datasheet/2/348/bh1750fvi-e-186247.pdf 

[4] Dfrobot. (n.d.-c). https://image.dfrobot.com/image/data/SEN0159/CO2b%20MG811%20datasheet.pdf 

[5] Karle, S., Bansode, V., Tambe, P., & Bhambare, R. (n.d.). (PDF) IOT based greenhouse monitoring system using Raspberry Pi. IoT Based Greenhouse Monitoring System Using Raspberry Pi. https://www.researchgate.net/publication/354297402_IoT_Based_Greenhouse_Monitoring_System_Using_Raspberry_Pi

[6] ChatGPT. (2025). AI-based text refinement for improved structure, readability, and formatting. OpenAI.

[7] Amazon. (n.d.). Environmental monitoring, light measurement, batteries, and boost converter devices. 

- BME280 Sensor: https://www.amazon.com/Atmospheric-Pressure-Temperature-Humidity-GY-BME280/dp/B0DHPCFXCK/
- BH1750 Light Sensor: https://www.amazon.com/HiLetgo-BH1750FVI-intensity-illumination-arduino/dp/B00M0F29OS/
- Eneloop Pro Batteries: https://www.amazon.com/Panasonic-BK-3HCCA8BA-eneloop-Pre-Charged-Rechargeable/dp/B00MXCIK32/
- MT3608 Boost Converter: https://www.amazon.com/AITRIP-Converter-Adjustable-Voltage-Regulator/dp/B0C858YYQ1/

[8] Elecfreaks. CO2 Monitoring Sensor
https://shop.elecfreaks.com/products/elecfreaks-octopus-co2-gas-sensor-mg811?srsltid=AfmBOoo9ZJgZG6MylX-AZjXNEBDBYNR3Z3_EC5a-3VQngJpJEwLPc0AH

[9] International Electrotechnical Commission (IEC). (1989). Degrees of Protection Provided by Enclosures (IP Code), IEC 60529. IEC.

[10] Liu, Y. (n.d.). Smart Greenhouse Monitoring and controlling based on ... Smart Greenhouse Monitoring and Controlling based  on NodeMCU . https://thesai.org/Downloads/Volume13No9/Paper_70-Smart_Greenhouse_Monitoring_and_Controlling.pdf 

[11] Abdul-Majid, M., Zahari, S. A., Othman, N., & Nadzri, S. (2024). Influence of technology adoption on farmers' well-being: Systematic literature review and bibliometric analysis. Heliyon, 10(2), e24316. https://doi.org/10.1016/j.heliyon.2024.e24316

[12] IGrow 800 environmental controller. Greenhouse Megastore. (n.d.). https://www.greenhousemegastore.com/collections/environmental-controls/products/igrow-800-environmental-controller?variant=42701245382855 

[13] WIFI greenhouse monitoring system with temperature & humidity alarms. ACF Greenhouses. (n.d.). https://www.acfgreenhouses.com/wifi-greenhouse-monitoring-system 

[14] Sensaphone 1800 Monitoring System w/NEMA 4X solid door enclosure FGD-1800-SD. Core & Main. (n.d.). https://supply.coreandmain.com/Sensaphone-1800-Monitoring-System-w-NEMA-4X-Solid-Door-Enclosure-FGD-1800-SD

[15] Alphasense O2-A3 Oxygen Sensor. Gaslab.com. (n.d.). https://gaslab.com/products/alphasense-02-a3-oxygen-sensor?currency=USD&utm_medium=cpc&utm_source=google&utm_campaign=Google+Shopping&variant=15400019165219 

[16] Eclipse F90 master environmental controller. Gothic Arch Greenhouses. (n.d.). https://www.gothicarchgreenhouses.com/eclipse-f90-master-environmental-controller 

[17] Monnit Wireless Sensor Systems. Long-range Wireless Sensors for Remote Monitoring. (n.d.). https://www.monnit.com/products/sensors/ 

[18] SunSenseTM controller. Ceres Greenhouse. (n.d.). https://ceresgs.com/sunsense-controller/ 

[19] EDYCARX CO2 Controller with temperature and humidity display day and night with relay function 15ft Ndir Sensor Cable, CO2 Controller for Grow Room, greenhouse, Grow Tent, home, office, factory : Patio, Lawn & Garden. (n.d.-b). https://www.amazon.com/EDYCARX-Dioxide-Controller-Function-Greenhouse/dp/B0BQR8GHR5 

[20] INKBIRD programmable CO2 Controller W/ S01 sensor ICC-500T. INKBIRD. (n.d.). https://inkbird.com/products/programmable-co-controller-icc-500t 

[21] Sensaphone 400 & 800 monitoring systems. Sensaphone. (n.d.). https://sensaphone.com/products/sensaphone-400-and-800-monitoring-systems/ 

[22] Industries, A. (n.d.). Waterproof 1-wire DS18B20 digital temperature sensor. adafruit industries blog RSS. https://www.adafruit.com/product/381?gQT=1 

Sources for Conditions and Constraints: 
- ASTM International.
- U.S. Department of Defense.
- International Electrotechnical Commission (IEC) 60529 Standard.
- National Electrical Manufacturers Association (NEMA) Standards Publication 250.
- Occupational Safety and Health Administration (OSHA) regulations.
- European Union Directive 2014/35/EU.
- National Fire Protection Association (NFPA) 70 – National Electrical Code (NEC).
- Underwriters Laboratories (UL) Standards.

## Statement of Contributions

Duy Tran – Gantt Chart, References, Introduction, Background, Specifications

Michael Feiel – Measures of Success, Resources, Github//Version Management

Henry Hurst – Formulating the Problem, Constraints, Specific, Budget, and Broader implications

Mohammed Almehmadi – Constraints, Broader Implications, Resources

All – Proofreading and Editing
