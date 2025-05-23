# Conceptual Design
## Introduction
A greenhouse is a controlled environment used to cultivate plants by regulating temperature, humidity, light, and other growing conditions, allowing for year-round cultivation while protecting crops from harsh weather, pests, and diseases. Accurate measurements inside a greenhouse are crucial for maintaining optimal plant health and productivity. Monitoring temperature prevents stress and ensures proper growth, while humidity control prevents mold and dehydration. Light levels must be measured to optimize photosynthesis, and CO₂ levels should be monitored to support plant development. Additionally, tracking soil moisture and pH helps maintain proper water and nutrient balance, preventing overwatering or nutrient deficiencies. By ensuring precise environmental conditions, greenhouse operators can optimize growth, improve yields, and efficiently manage resources through automation and troubleshooting.

In today’s rapidly advancing technological landscape, the demand for portable, efficient, and data-driven monitoring systems is more prevalent than ever. The proposed project aims to develop a robust, modular solution designed to collect, process, and transmit data wirelessly, all while maintaining portability and operational reliability. The system’s primary objective is to seamlessly integrate hardware and software components into a cohesive framework capable of continuous data monitoring and real-time reporting.

To meet stakeholder expectations and align with industry standards, the system will incorporate modular hardware units powered by battery sources, minimizing cable dependency and enhancing mobility. These modules will transmit data wirelessly to a central processor, which will then update a cloud-based platform when a stable Wi-Fi connection is available. Additionally, the system will feature local data storage to ensure no loss of information during network outages, thereby maintaining data integrity and availability.

The conceptual design process will focus on defining clear requirements, decomposing the system into atomic subsystems, and addressing all relevant constraints. Through comparative analysis, potential solutions will be evaluated to determine the most viable approach, with an emphasis on efficiency, scalability, and user accessibility. This document provides the project’s high-level solution, including hardware architecture, operational flow, and subsystem specifications, while also addressing ethical, professional, and regulatory considerations.
## Fully Formulated Problem
The primary objective of this project is to develop a portable, modular data collection and transmission system that operates reliably in various environments. The system shall consist of lightweight, battery-powered modules capable of gathering data and wirelessly transmitting it to a central processing unit. The central processing unit shall manage data aggregation and update a cloud-based platform in real-time when a stable Wi-Fi connection is available. In the event of network unavailability, the system shall store collected data locally to ensure data preservation and continuity.
### Portable Sensor Network Specifications: 
1. Portability and Compactness: Modules shall be lightweight and compact to facilitate mobility and ease of deployment.
   - Sensor Units: Modules shall monitor and record temperature, humidity, light intensity, CO₂, and oxygen levels across multiple locations.
   - Unit Chassis: The unit housing shall withstand greenhouse environmental conditions, including high humidity and dust.
2. Battery Operation: Modules shall be battery-powered to eliminate dependency on fixed power sources.
   - Battery Lifespan: Batteries shall be able to operate for minimum of 72 hours before recharging.
   - Battery Safety Standard: The system shall not exceed 50V operating voltage to comply with OSHA regulations.
   - Power Converter and Electrical Components: The power converter and electrical components shall be designed for safe operation in greenhouse conditions to prevent electrical hazards	
3. Power Monitoring: Each module shall track its battery level and alert users when recharging or replacement is necessary.
4. Wireless Data Transmission: Collected data shall be transmitted wirelessly from each module to the central processor for real-time monitoring.
5. Cloud Integration: The central processor shall transmit data to a cloud platform when Wi-Fi connectivity is available.
6. Offline Data Storage: In the absence of network connectivity, modules shall store data locally to ensure no data loss for offloading.
7. Data Visualization and Retention: The cloud platform shall display live data and retain historical data for analysis and monitoring.
   - Website Interface: The graphic user interface shall provide a web-based dashboard for data visualization and remote access.
8. Camera: The central processing unit shall integrate a camera system for plant growth tracking.

These requirements have been established in collaboration with stakeholders to address functional needs while complying with industry standards and best practices. The design will also account for ethical, safety, and environmental considerations to minimize risks and enhance system sustainability.

### Constraints:
- Environmental Conditions (IP67) and RoHS: To ensure reliability in high-humidity, dust-prone environments (IEC 60529 Standard).
  - IP65 or higher for protection against dust and low-pressure water jets.
  - IP67 if additional submersion resistance is required.
  - The enclosures shall comply with NEMA 4X as an alternative to IP ratings, providing dust-tight, watertight, and corrosion-resistant enclosures.
  - The materials used in enclosures and components shall comply with ASTM B117 for salt fog resistance in corrosion-prone areas.
  - Restriction of Hazardous Substances (RoHS) standards for environmental sustainability pertaining to PCB materials. 
- Power Limitations (50V max): To comply with OSHA regulations for electrical safety (29 CFR CFR 1910 Subpart S, 29 CFR 1910.1200, 29 CFR 1910.1000, and 29 CFR 1910.39).
  - OSHA 29 CFR 1910.39 for electrical safety in wet/damp locations such that the subsystems are flame-retardant.
  - OSHA 29 CFR 1910.1200 pertaining to to hazardous communication such that the device does not affect the soil and plants from the combo-power and sensor unit subsystem. 
  - 50V or lower DC systems classified as "low voltage" per OSHA standards.
  - OSHA 29 CFR 1910 Subpart S for Sensor Unit pertaining to electrical safety.
  - OSHA 29 CFR 1910.1000 pertaining to the emmitance of air contaminants from the power and sensor subsystem. 
- Safety and Regulatory Compliance (NEC, UL): To prevent electrical hazards and ensure safe operation (NEC Article 547, NEC 210.8(B), NEC 250.32, UL 943, UL 1449).
- Sensor and Actuator Integration: To ensure accurate responses based on environmental data.
## Comparative Analysis of Potential Solutions
Greenhouse monitoring systems are essential for maintaining optimal growing conditions and maximizing crop yield. Currently available solutions range from DIY approaches to industrial-grade systems, each with its own advantages and disadvantages. Below, we analyze multiple existing solutions to determine their suitability for solving the problem at hand.

#### DIY Solutions
DIY greenhouse monitoring systems are commonly showcased in online tutorials and videos, providing basic environmental monitoring at a low cost. These systems typically involve using off-the-shelf components such as Arduino or Raspberry Pi boards combined with sensors for temperature, humidity, and soil moisture.

Advantages:
- Low Cost: Affordable components make these systems budget friendly.
- Customizability: The flexible design options allow for tailored solutions to meet specific needs.
- Educational Value: Building a DIY system offers valuable hands-on experience.
Disadvantages:
- Lack of Accuracy and Durability: These systems are often built with inexpensive sensors, which can diminish in performance over time.
- High Maintenance: They require regular adjustments and troubleshooting to stay operational.
- Limited Data Management: Typically lacks advanced data processing and cloud integration.
#### Industrial Solutions
Industrial-grade greenhouse monitoring systems offer comprehensive and precise data, tailor-made for large-scale commercial operations. Below is the analysis of some notable options: 
1. **iGrow 800 Environmental Controller**

   - **Cost:** $4,145.00

   - **Pros:** Provides advanced environmental monitoring for temperature, humidity, and CO₂.

   - **Cons:**
      - High cost makes it impractical for small to mid-sized greenhouses.
      - Does not include oxygen monitoring.
      - Its complexity may necessitate specialized training.
2. **WIFI Greenhouse Monitoring System from ACF Greenhouses**
   - **Cost:** $69.00
   - **Pros:** Affordable and simple to set up.
   - **Cons:
     - Limited functionality, lacking advanced features like oxygen monitoring and light
intensity sensors.
      - Data coverage can be inconsistent due to Wi-Fi reliance.
      - Not portable for offline use.
3. **Sensaphone 1800 Monitoring System**
   - **Cost:** $1,014.95
   - **Pros:** Monitors up to 8 environmental conditions.
   - **Cons:**
      - High initial cost.
      - Primarily focused on monitoring without automation capabilities.
      - Requires telephone lines, which limits portability.   
4. **ECLIPSE F90 Master Environmental Controller**
   - **Cost:** Varies
   - **Pros:** Offers precise control of temperature, humidity, and CO₂ levels.

   - **Cons:**
      - Complex setup requiring technical knowledge.
      - Lacks monitoring for oxygen and light intensity.
      - No offline data portability.   
5. **Monnit Wireless Sensor Systems**
   - **Cost:** Varies based on configuration
   - **Pros:** Provides comprehensive wireless monitoring for multiple environmental factors.
   - **Cons:**
      - Can become expensive, especially with multiple sensors.
      - Wireless connectivity may be unreliable in dense greenhouse environments.
      - Lacks offline data collection and oxygen monitoring.   
6. **Ceres SunSense™ Controller**
   - **Cost:** Custom pricing
   - **Pros:** Advanced monitoring capabilities including temperature, humidity, CO₂, and PAR tracking.
   - **Cons:**
      - High cost and steep learning curve.
      - No oxygen monitoring or offline data offloading.  
7. **EDYCARX CO₂ Controller**
   - **Cost:** Approximately $300
   - **Pros:** Effectively monitors CO₂, temperature, and humidity.
   - **Cons:**
      - Focused on CO₂ regulation, requiring supplementary systems for complete monitoring.
      - Lacks light intensity and oxygen concentration monitoring.   
8. **INKBIRD CO₂ Controllers**
   - **Cost:** Ranges from $100 to $400

   - **Pros:** Maintains optimal CO₂ levels for plant growth.
   - **Cons:**
      - Limited in scope, primarily focused on CO₂ monitoring.
      - No comprehensive environmental control or offline data capabilities.   
9. **Sensaphone 400 Monitoring System**
   - **Cost:** $455.00
   - **Pros:** Efficiently monitors four environmental conditions.
   - **Cons:**
      - Limited to only four monitoring points, which may not suit larger greenhouses.
      - No light intensity or oxygen monitoring.
      - Lacks offline data portability.
#### Analysis and Selection

Current solutions often lack modularity and scalability or are too costly for small to medium-sized greenhouse operations. Furthermore, many systems fall short in offering critical features such as oxygen monitoring, light intensity tracking, and offline data management, which are essential for effective and flexible greenhouse management.

After evaluating the advantages and disadvantages of existing systems, it becomes clear that a new solution must address the following gaps:
1. **Affordability and Scalability:** Designed to be suitable for small to mid-sized operations.
2. **Modular and Customizable Design:** Allowing users to tailor the system to meet their specific needs.
3. **Comprehensive Environmental Monitoring:** Covering temperature, humidity, CO₂, oxygen, and light intensity.
4. **Offline Data Portability:** Ensuring data collection remains functional even without Wi-Fi connectivity.
5. **Ease of Use and Maintenance:** Requiring minimal technical expertise for installation and operation.

By integrating these features into a single hybrid solution, the proposed system aims to bridge the gap between DIY and industrial options, delivering a cost-effective, modular, and robust monitoring system that caters to the diverse needs of greenhouse applications.

## High-Level Solution
The proposed portable sensory network will consist of three remote units utilizing ESP32 microcontrollers and a Raspberry Pi as the central control unit. Each remote unit will aggregate data from five sensors—CO2, oxygen, humidity, light intensity, and temperature. These units’ encasement will be 3d printed with PETG filament to ensure moisture and temperature resistance to the box. Once the data is recorded, it will be sent to the central processing unit (Raspberry Pi) for cloud uploading and data storage via Wi-Fi. The ESP boards and Raspberry Pi are Wi-Fi compatible, so its functionalities will be used. Each individual unit will be powered by batteries with a boost converter to maintain a consistent 3.3 volts.  The central processing unit will receive its power from a standard 5-volt power supply. After the data is processed, it will be uploaded to the cloud for interfacing through a dedicated website. This website will provide a dashboard view of each of the remote units along with their respective sensor readings. 

### Hardware Block Diagram
 
<img src="resources/concept-block-diagram.png" alt="Block Diagram" width="auto" height="auto"> 

### Operational Flowchart
 

<img src="resources/concept-flow-chart.png" alt="Flow Chart" width="auto" height="auto"> 

#### Key Features
1. Modularity and Scalability:
   - The system will support the addition of new sensors without requiring significant reconfiguration.
   - The modular design will allow users to tailor the system to their specific needs, whether for small-scale or commercial applications.
2. Wireless Data Transmission and Local Storage:
   - Sensor data will be transmitted via Wi-Fi or MQTT protocols to a central Raspberry Pi unit.
   - In the event of a connectivity failure, data will be stored locally on the Raspberry Pi and uploaded once the connection is restored.
   - The system will support offline data portability through USB or SD card transfer.
3. Data Integrity and Reliability:
   - Data consistency checks will ensure that sensor readings remain within expected ranges, detecting any anomalies or sensor drift.
   - Regular calibration routines will maintain accuracy, comparing sensor outputs to known standards.
   - Redundant sensors will be deployed in critical areas to cross-verify measurements.
4. User-Friendly Interface and Real-Time Monitoring:
   - A web-based dashboard will display real-time data and historical trends.
   - Customizable alerts will notify users of environmental anomalies via email or mobile notifications.
   - User access levels will be configurable, allowing administrators to grant or restrict access to specific features.
5. Power Efficiency and Durability:
   - Low-power components and sleep mode functionality will optimize battery life.
   - Rugged enclosures will protect sensors from moisture, dust, and temperature extremes, maintaining reliability in greenhouse environments.
6. Seamless Data Management and Analytics:
   - Data will be logged and timestamped to allow trend analysis and prediction.
   - The system will provide downloadable CSV files for integration with third-party analytics software.
________________________________________

#### Evaluation and Success Criteria
To ensure the system's effectiveness and reliability, the following key performance indicators (KPIs) and testing methodologies will be employed:
1. Accuracy and Reliability:
   - Calibration testing will compare sensor readings against reference devices.
   - Environmental stress testing will assess stability and accuracy under varying conditions.
   - Success Metric: Sensor deviation of less than ±2% from reference standards.
2. Data Transmission and Integrity:
   - Wireless range tests will evaluate the distance and stability of data transmission.
   - Offline data storage tests will verify uninterrupted logging during connectivity loss.
   - Success Metric: 100% data retention and less than 1-second latency during transmission.
3. Power Efficiency:
   - Discharge tests will determine battery life under normal operation.
   - Power profiling will identify any components with high energy consumption.
   - Success Metric: Minimum of 12 hours of battery life under continuous operation.
4. System Durability:
   - Moisture and temperature endurance tests will simulate real-world conditions.
   - Drop tests will verify enclosure durability and component security.
   - Success Metric: No loss of functionality after 24-hour exposure to high humidity and temperature extremes.
5. User Experience:
   - User testing will gather feedback on setup, usability, and data interpretation.
   - Interface testing will ensure real-time data visualization and intuitive controls.
   - Success Metric: Positive user feedback on ease of use and data clarity.
6. Cost-Effectiveness and Scalability:
   - Comparative cost analysis will benchmark the solution against commercial systems.
   - Modular expansion tests will verify that additional sensors do not degrade performance.
   - Success Metric: System cost 50-70% lower than comparable industrial solutions.
________________________________________

By implementing this high-level solution, the system will effectively bridge the gap between expensive industrial monitoring solutions and affordable DIY alternatives, delivering reliable and scalable environmental monitoring for a wide range of greenhouse applications. 

## Atomic Subsystem Specifications

**Sensor Units**

The individual sensor units will communicate data to the central processing unit wirelessly via Wi-Fi. Each remote sensor unit will have its own device identifier to ensure that the central processing unit does not receive information from multiple devices, preventing data from being overwritten. As sensors collect real-time data, this information will be sent to the Raspberry Pi for integration with the website dashboard. In offline scenarios, the collected data can be stored on an SD card for later retrieval 

  - Functions: Data acquisition, wireless transmission, local storage.
  - Inputs: Sensor data, battery voltage.
  - Outputs: Wireless data (Wi-Fi).
  - Interfaces: Sensor data (digital, analog), battery power, Wi-Fi.
  - Shall measure temperature, humidity, light, CO2, and O2. 
  - Shall” transmit data every 5 minutes when Wi-Fi is available and unavailable. 
  - Shall timestamp each sample using synchronized Wi-Fi connection. 
  - Shall store data in internal SD card until overwriting oldest data.

**Central Processing Hub (Raspberry Pi 4)**

- Functions: Data processing, storage, web interface.
- Inputs: Wireless data (Wi-Fi).
- Outputs: Web dashboard, data offloading, time synchronization (Wi-Fi).
- Interfaces: Wi-Fi, USB.
- Shall store sensor data in a database. 
- Shall host a web server for data visualization. 
- Shall allow data offloading via USB.

**Monitoring Dashboard**

  - Web Dashboard: 
  - Functions: Data visualization, user interface, store data in .xslx.
  - Inputs: Database data, camera feed.
  - Outputs: User interface, .xlsx download.
  - Interfaces: Web browser.
  - Shall display real time and historical data. 
  - Shall provide user authentication. 
  - Shall display camera feed.
  - Shall store and output an excel file upon request.

 **Real-Time Monitoring Unit**

  - Camera System: 
  - Functions: image capture, image storage.
  - Inputs: Raspberry Pi trigger.
  - Outputs: Image files.
  - Interfaces: Raspberry Pi camera port.
  - Shall take a photo every hour. Shall store photos on the Raspberry Pi.

## Ethical, Professional, and Standards Considerations

- Environmental Impact: The system promotes efficient resource management in greenhouses, reducing waste. This has implications for local food security, reducing dependency on imports and strengthening regional food systems.  
- Long-Term Cost Considerations: While the system may increase initial power usage, optimizing energy efficiency and automating data collection could lead to long-term savings by improving resource management and reducing manual labor.
- Safety: Adherence to electrical safety standards (OSHA, NEC, UL) ensures safe operation. Such risks involve electricity, structure, and gases.
- Data Privacy: User authentication and access control protect sensitive data.

IEC 60529 (IP67/IP68 Rating):
- Ensures enclosures are resistant to dust and water ingress.
- Helps maintain device function in high humidity greenhouse environments.

NEMA 250 (Type 4X Enclosure):

- Equivalent to IP ratings but includes corrosion resistance.
- Ensures electrical enclosures can withstand greenhouse conditions.

ASTM B117:

- Ensures corrosion resistance of enclosure materials, especially in high humidity greenhouses.

OSHA 29 CFR 1910.303:

- Provides general electrical safety standards, for example max 50V DC.
- Ensures safe operating voltage and insulation for user protection.

OSHA 29 CFR 1910.307:

- Addresses requirements for electrical systems in wet/damp locations.
- Ensures safe installation of equipment in greenhouse environments.

NEC Article 547:

- Specifies electrical design and installation for agricultural buildings.
- Ensures system wiring and grounding is greenhouse compliant.

NEC 210.8(B):

- Requires GFCI protection for outlets in wet/damp environments.
- Helps prevent electrical shock hazards near watering systems.

NEC 250.32:

- Covers grounding of separate buildings/structures.
- Ensures electrical safety if greenhouse and control unit are in different buildings.

UL 943:

- Certifies ground-fault protection devices.
- Ensures protection from electrical shocks in damp zones.

UL 1449:

- Certifies devices that protect from voltage spikes.
- Helps protect electronics during lightning or power fluctuations.

## Resources

| Item | Description | Quantity | Cost |
|------|-------------|----------|------|
| Raspberry Pi | Central Microcontroller | 1 | $35 |
| ESP-WROOM-32 | Sensors Microcontroller | 3 | $12 per 4|
| Eneloop Pro | Batteries | 16 | $36.45 per 8 |
| BME280 | Humidity Sensor | 3 | $15.99 per 2 |
| BH1750 | Light Measurement | 3 | $7.49 per 3 |
| SCD40 | CO₂ Monitoring | 3 | $21.94|
| MT3608 | Boost Converter | 3 | $5.99 per 5 |
| Gravity O2 Sensor | Oxygen Sensor | 3 | $55 |
| 3D Printing Plastic Filaments | Used for Case Prototype | 3 | $12.99 |
| DS18B20 | Temperature Sensor | 3 | $9.95 |
| Go Pro | Visual Feed | 1 | $20.00 |

  - Sensor Nodes: $400 (sensors, ESP32, enclosures, batteries).
  - Raspberry Pi 4: $100 (Pi, camera, power supply).
  - Total: $500.

- Division of Labor: 
  - Duy Tran: Sensor Node Design, Sensor Integration.
  - Michael Feiel: Wi-Fi Interfacing, Software Development, Web Dashboard.
  - Henry Hurst: Camera System, Enclosure Design.
  - Mohammed Almehmadi: Power Management.
- Timeline: 

<img src="resources/gantt-chart.png" alt="Gantt Chart" width="auto" height="400"> 
 

References:
- [1] DATASHEET raspberry pi 4 model B. (n.d.). https://datasheets.raspberrypi.com/rpi4/raspberry-pi-4-datasheet.pdf 
- [2] Adafruit. (n.d.-a). https://cdn-learn.adafruit.com/assets/assets/000/115/588/original/bst-bme280-ds002.pdf?1664822559= 
- [3] Digital 16bit serial output type ambient light sensor IC. (n.d.-c). https://www.mouser.com/datasheet/2/348/bh1750fvi-e-186247.pdf 
- [4] Dfrobot. (n.d.-c). https://image.dfrobot.com/image/data/SEN0159/CO2b%20MG811%20datasheet.pdf 
- [5] Karle, S., Bansode, V., Tambe, P., & Bhambare, R. (n.d.). (PDF) IOT based greenhouse monitoring system using Raspberry Pi. IoT Based Greenhouse Monitoring System Using Raspberry Pi. https://www.researchgate.net/publication/354297402_IoT_Based_Greenhouse_Monitoring_System_Using_Raspberry_Pi
- [6] ChatGPT. (2025). AI-based text refinement for improved structure, readability, and formatting. OpenAI.
- [7] Amazon. (n.d.). Environmental monitoring, light measurement, batteries, and boost converter devices. 
  - BME280 Sensor: https://www.amazon.com/Atmospheric-Pressure-Temperature-Humidity-GY-BME280/dp/B0DHPCFXCK/
  - BH1750 Light Sensor: https://www.amazon.com/HiLetgo-BH1750FVI-intensity-illumination-arduino/dp/B00M0F29OS/
  - Eneloop Pro Batteries: https://www.amazon.com/Panasonic-BK-3HCCA8BA-eneloop-Pre-Charged-Rechargeable/dp/B00MXCIK32/
  - MT3608 Boost Converter: https://www.amazon.com/AITRIP-Converter-Adjustable-Voltage-Regulator/dp/B0C858YYQ1/
- [8] Elecfreaks. CO2 Monitoring Sensor: https://shop.elecfreaks.com/products/elecfreaks-octopus-co2-gas-sensor-mg811?srsltid=AfmBOoo9ZJgZG6MylX-AZjXNEBDBYNR3Z3_EC5a-3VQngJpJEwLPc0AH
- [9] International Electrotechnical Commission (IEC). (1989). Degrees of Protection Provided by Enclosures (IP Code), IEC 60529. IEC.
- [10] Liu, Y. (n.d.). Smart Greenhouse Monitoring and controlling based on ... Smart Greenhouse Monitoring and Controlling based  on NodeMCU . https://thesai.org/Downloads/Volume13No9/Paper_70-Smart_Greenhouse_Monitoring_and_Controlling.pdf 
- [11] Abdul-Majid, M., Zahari, S. A., Othman, N., & Nadzri, S. (2024). Influence of technology adoption on farmers' well-being: Systematic literature review and bibliometric analysis. Heliyon, 10(2), e24316. https://doi.org/10.1016/j.heliyon.2024.e24316
- [12] IGrow 800 environmental controller. Greenhouse Megastore. (n.d.). https://www.greenhousemegastore.com/collections/environmental-controls/products/igrow-800-environmental-controller?variant=42701245382855 
- [13] WIFI greenhouse monitoring system with temperature & humidity alarms. ACF Greenhouses. (n.d.). https://www.acfgreenhouses.com/wifi-greenhouse-monitoring-system 
- [14] Sensaphone 1800 Monitoring System w/NEMA 4X solid door enclosure FGD-1800-SD. Core & Main. (n.d.). https://supply.coreandmain.com/Sensaphone-1800-Monitoring-System-w-NEMA-4X-Solid-Door-Enclosure-FGD-1800-SD
- [15] Alphasense O2-A3 Oxygen Sensor. Gaslab.com. (n.d.). https://gaslab.com/products/alphasense-02-a3-oxygen-sensor?currency=USD&utm_medium=cpc&utm_source=google&utm_campaign=Google+Shopping&variant=15400019165219 
- [16] Eclipse F90 master environmental controller. Gothic Arch Greenhouses. (n.d.). https://www.gothicarchgreenhouses.com/eclipse-f90-master-environmental-controller 
- [17] Monnit Wireless Sensor Systems. Long-range Wireless Sensors for Remote Monitoring. (n.d.). https://www.monnit.com/products/sensors/ 
- [18] SunSenseTM controller. Ceres Greenhouse. (n.d.). https://ceresgs.com/sunsense-controller/ 
- [19] EDYCARX CO2 Controller with temperature and humidity display day and night with relay function 15ft Ndir Sensor Cable, CO2 Controller for Grow Room, greenhouse, Grow Tent, home, office, factory : Patio, Lawn & Garden. (n.d.-b). https://www.amazon.com/EDYCARX-Dioxide-Controller-Function-Greenhouse/dp/B0BQR8GHR5 
- [20] INKBIRD programmable CO2 Controller W/ S01 sensor ICC-500T. INKBIRD. (n.d.). https://inkbird.com/products/programmable-co-controller-icc-500t 
- [21] Sensaphone 400 & 800 monitoring systems. Sensaphone. (n.d.). https://sensaphone.com/products/sensaphone-400-and-800-monitoring-systems/ 
- [22] Industries, A. (n.d.). Waterproof 1-wire DS18B20 digital temperature sensor. adafruit industries blog RSS. https://www.adafruit.com/product/381?gQT=1

Sources for Standards:
- [1] ASTM International. (n.d.). Environmental sensor standards. ASTM. 
- [2] U.S. Department of Defense. (n.d.). Defense Standardization Program (DSP). Defense Logistics Agency. https://www.dsp.dla.mil/
- [3] International Electrotechnical Commission. (2013). IEC 60529: Degrees of protection provided by enclosures (IP Code). IEC Webstore.   https://webstore.iec.ch/en/publication/2452
- [4] National Electrical Manufacturers Association. (2020). ANSI/NEMA 250-2020 – Enclosures for Electrical Equipment (1000 Volts Maximum). American National Standards Institute. https://webstore.ansi.org/standards/nema/ansinema2502020
- [5] Occupational Safety and Health Administration. (n.d.). Standard 1910.303 – General Requirements. OSHA. https://www.osha.gov/laws-regs/regulations/standardnumber/1910/1910.303
- [6] Occupational Safety and Health Administration. (n.d.). Standard 1910.307 – Hazardous (Classified) Locations. OSHA. https://www.osha.gov/laws-regs/regulations/standardnumber/1910/1910.307
- [7] European Union. (2014). Directive 2014/35/EU – Low Voltage Directive. EUR-Lex. https://eur-lex.europa.eu/eli/dir/2014/35/oj/eng
- [8] National Fire Protection Association. (2023). NFPA 70 – National Electrical Code. NFPA. https://www.nfpa.org/codes-and-standards/nfpa-70-standard-development/70
- [9] Underwriters Laboratories. (n.d.). UL Standards Catalog. UL. https://www.ul.com/resources/apps/standards-catalog



## Statement of Contributions
- Duy Tran: Sensor Node Design, Document Editing.
- Michael Feiel: Web Dashboard, Software Development, Flowchart, Block Diagram.
- Henry Hurst: Raspberry Pi Integration, Camera System, Enclosure Design.
- Mohammed Almehmadi:  Constraint Research, Power Management.

