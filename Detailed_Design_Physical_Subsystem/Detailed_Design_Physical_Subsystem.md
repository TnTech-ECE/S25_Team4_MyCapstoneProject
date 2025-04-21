# Physical Detailed Design

This document presents a comprehensive overview of the Physical Subsystem, one of the four key components of the greenhouse monitoring solution—the others being the Power Subsystem, Central Processing Hub Subsystem, and Mechanical Subsystem. The Physical Subsystem is on the lower end of the components but requires a decent about of tinkering to get accurate. The document further outlines the technical constraints, relevant industry standards, and operational limitations that influence the design and deployment of the Physical Subsystem. Lastly, it details the step-by-step procedure for constructing and implementing the subsystem as part of the overall greenhouse monitoring solution.
## Function of the Subsystem

The Remote Box Cases play a crucial role in the greenhouse monitoring system by holding all the other subsystems together, providing a ease of access to components, and ease of mobile movement of the boxes. Each box will contain ESP-WROOM-32 microcontroller, printed circuit board (PCB), BME280 sensor (which measures relative humidity, barometric pressure, and ambient temperature), BH1750 (used for light intensity measurement), SCD40 (dedicated to CO₂ monitoring), Gravity Electrochemical Oxygen Sensor (for detecting oxygen levels), and a battery connection box (four batteries). These Remote Box Cases will be made out of PETG filament to ensure moisture and temperature resistance to the box.

## Specifications and Constraints

The physical enclosure for the sensor subsystem shall be designed to house the ESP-WROOM-32 microcontroller and its associated environmental sensors (BME280, BH1750, SCD40, and Gravity Electrochemical Oxygen Sensor) in a compact, durable, and functional case. The case must support the sensor array's environmental monitoring function while ensuring mechanical protection, proper sensor exposure, and system longevity within the greenhouse setting.
Design Specifications:

-	Component Housing:
The case shall securely accommodate a custom PCB with the ESP-WROOM-32 and all associated sensors. The internal geometry must account for component dimensions, connector clearances, and mounting standoffs.
 -	Sensor Accessibility:
Openings or breathable membranes must be integrated to allow unobstructed sensing of environmental variables:
  -	Perforated vent area for temperature, humidity, and pressure (BME280)
  -	Transparent or translucent window for light intensity sensing (BH1750)
  - Direct air exposure ports for gas sensors (SCD40 and Oxygen sensor), while preventing debris ingress
-	Material Selection:
The enclosure shall be constructed from UV-resistant, corrosion-resistant, and RoHS-compliant plastics (e.g., ASA, ABS, or PC blends). Materials must be non-reactive and safe for prolonged greenhouse use.
-	Ingress Protection:
The case shall achieve at least IP54 rating to guard against dust accumulation and water splashes, while still allowing necessary airflow for accurate environmental readings.
-	Mounting & Placement:
The design shall feature integrated mounting flanges or slots for zip ties or screws, enabling secure attachment to greenhouse infrastructure (e.g., poles or walls). The orientation must support optimal sensor function and wireless signal strength.
-	Thermal Management:
Passive ventilation shall be included to prevent internal heat buildup, especially around the microcontroller and sensors sensitive to temperature deviations.
-	Assembly & Maintenance:
The enclosure shall use snap-fit mechanisms or minimal fasteners for ease of assembly and field maintenance. Design shall allow access to the PCB for diagnostics or upgrades without compromising structural integrity.






