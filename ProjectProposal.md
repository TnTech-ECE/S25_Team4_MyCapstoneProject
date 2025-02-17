# Project Proposal

## Introduction

As technology advances, its integration with agriculture follows. One such application is for greenhouses. Essentially, greenhouses are buildings used to grow plants in a controlled environment. This project proposal is to design a portable sensory network to detect and control CO<sub>2</sub>, O<sub>2</sub>, light, temperature, and humidity. There will also be camera implementation to show plant growth through time.

## Formulating the Problem

Greenhouses can have inaccurate measures of temperature causing issues with plant growth. The group is to work with Dr. Kenmonth-Schultz, as well as the biological department at Tennessee Tech, to make a sensory network that is capable of detecting specific variables mentioned above and regulating the temperature and optional water pumps, fan speeds, and ventilation angles. Website Design, hardware implementation, and running wires requires a diverse set of engineers and minds to engineer a solution to these problems. All solutions that are currently available have soaring prices, and other specific devices might be required. There seems to be no all-in-one solution for this application.

### Background

The problem identified affects Tennessee Tech’s Biology department specializing in botany. The problem with the pre-existing greenhouse solution lies in the element used to gather information for attaining data within the greenhouse. A current problem with greenhouses is that sensors do not sense a gradient of temperature and humidity levels. This is due to their installation locations being primarily stationary. The challenges with this project pertain to the multi-faceted aspects of the project dealing in power, sensors, actuators, and familiarity in biological systems. Off-the shelf solutions are not sufficient in that there are many difficulties in attaining prices of the portable system for these sensors. 

### Specifications

Size should be lightweight, and everything will need to fit in a small space. Also, power in a portable device will be limited, and several components will need power that needs to be minimized. Modules shall be powered via ethernet connection, while the modules’ data shall be transmitted wirelessly to a central processor. The processor shall transmit, via WiFi, to update a website with live data. There shall also be some degree of data storage. The live website shall have controls for the system, which shall be able to change desired parameters for CO<sub>2</sub>, O<sub>2</sub>, light, temperature, and humidity. The system shall also automatically control CO<sub>2</sub>, O<sub>2</sub>, temperature, and humidity through the use of opening or closing the greenhouse flaps, activation or deactivation of fans, and activation or deactivation of the present humidity system (whether that be a humidifier, a water pump, or sprinkler system).


### Constraints
 
The environment of the green house will be a challenge because the device must work in an environment that will be affected by water, dust, and humidity. So, the device will be made as efficient as possible in this environment. The required power shall not exceed 50 V according to occupational safety and health administration. Additionally, the sensor network must interface properly with given actuators depending on data ascertained. As such, the actuation circuits shall have circuit protection against overloads in the case of a fire. Our solution shall also comply with NEC regulations requiring GFCI protection for outlets supplying horticultural lighting with flexible cords. 

## Survey of Existing Solutions

Many DIY videos of a similar caliber are present on YouTube. Additionally, a few companies dedicated to industrial-grade sensors and software offer similar solutions. The “backyard greenhouse” designs seem too small-scale, while the industrial-grade setup is too pricy for a project this size. This project aims to sit right between the two scales, being usable for a medium-sized greenhouse project.

## Measures of Success

The project’s success will be measured by the system’s usability in a greenhouse setting. Specific successes will include sensor accuracy, data acquisition, power efficiency, and meeting customer expectations. The ability for the website to store and modify the system will be an additional measure of success.

## Resources

This project will require multiple sensors for various elements, such as CO<sub>2</sub>, humidity, sunlight, and temperature. These sensors will need to receive power via ethernet cable and transmit their data wirelessly to a central processing unit. This unit will then upload the data to a live webpage that can monitor and manually control modules. The protocol that will be used for the sensor network will be MQTT which allows the sensors to communicate over a network with limited bandwidth. 

### Budget

The bulk cost of the project will be in attaining multiple sensors, and ethernet cable for use in power over ethernet. Sensors will be in the range of $7-$20, Ethernet cables will be around $10 per every 50 feet. In addition to this a Raspberry Pi 4 will be $35. For usage in power over Ethernet, a PoE switch is required which costs around $100. Since there will be many sensors and many ethernet cables, we can safely round out the estimated budget to cap out at $1000. 

### Personnel

The team has similar experience overall but can learn the necessary knowledge to complete the project. Every individual on the team has completed the pre-requisite courses in the Electrical Engineering curriculum, giving a solid understanding of learning new materials and design. In addition, some members have completed internships giving those members practical experience in teamwork. 
 
### Timeline

![Gantt Chart](https://github.com/TnTech-ECE/S25_Team4_MyCapstoneProject/blob/6b491942bbbfa6d045a560bc66826962298cc58d/gantt-chart.png) 

## Specific Implications

The implications of the implementation of the greenhouse sensor network are accurate data acquisition tools, visual feed of growth time, and regulation of temperatures. The general user shall receive data easily and effectively, and the temperature regulation shall gather info from the greenhouse. 

## Broader Implications

One of the main economic impacts is power. Our system will draw more power; however, using sleep modes on certain sensors or cameras will draw less power to the system. Another impact is the wiring and sensors within the greenhouse. There is a potential chance it will affect the greenhouse in unexpected ways and give errors to the sensors with the high humidity.

## References

DATASHEET raspberry pi 4 model B. (n.d.). https://datasheets.raspberrypi.com/rpi4/raspberry-pi-4-datasheet.pdf 

Adafruit. (n.d.-a). https://cdn-learn.adafruit.com/assets/assets/000/115/588/original/bst-bme280-ds002.pdf?1664822559= 

Digital 16bit serial output type ambient light sensor IC. (n.d.-c). https://www.mouser.com/datasheet/2/348/bh1750fvi-e-186247.pdf 

Dfrobot. (n.d.-c). https://image.dfrobot.com/image/data/SEN0159/CO2b%20MG811%20datasheet.pdf 

Karle, S., Bansode, V., Tambe, P., & Bhambare, R. (n.d.). (PDF) IOT based greenhouse monitoring system using Raspberry Pi. IoT Based Greenhouse Monitoring System Using Raspberry Pi. https://www.researchgate.net/publication/354297402_IoT_Based_Greenhouse_Monitoring_System_Using_Raspberry_Pi 

## Statement of Contributions

Duy Tran – Gantt Chart, References, Introduction, Background, Specifications

Michael Feiel – Measures of Success, Resources, Uploading to Github

Henry Hurst – Formulating the Problem, Constraints, Specific and Broader implications

Mohammed Almehmadi – Constraints, Broader Implications, Automation, Resources
