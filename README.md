# Assembly Instructions 

<!-- ![Alt Text](https://github.com/cellworld/robot_assembly/blob/master/robot_overview.png) -->
<p align="center">
  <img src="https://github.com/cellworld/robot_assembly/blob/master/images/robot_overview.png" alt="robot_overview" width="600" height="200">
</p>


## 3D printed parts
* chassis.stl 
* pump_holder.stl
* motor_stopper.stl
* motor_platform.stl
* lever_arm.stl
* cam.stl

## Robot and aversive puff parts
* **Plastic gearmotor** (Gearmotor and Encoder Assembly for Romi/TI-RSLK MAX, Pololu, Las Vegas, Nevada, USA, part no. 3675)
* **Motor shaft adapter** ( Pololu Universal Aluminum Mounting Hub for 3mm Shaft, M3 Holes (2-Pack), Pololu, Las Vegas, Nevada, USA, part no. 1996)
* **Valve stem extender** (2-Pack Tire Valve Extension 45 Degree, LEEGAWU)
* **16g CO2 canister and inflator** (Ultraflate, Genuine Innovations, San Luis Obispo, CA, USA)
* **Drivetrain motor** (Geared DC Motor with Magnetic Encoder Outputs - 7 VDC 1:20 Ratio, Adafruit, New York, NY, USA, part no. 4416)
* **Battery** 7.4V (7.4V 1000mAh Odamiya Plug Lithium Battery, PUOO)
* **Track set** (Pololu 22T Track Set - Black, Pololu, Las Vegas, Nevada, USA, part no. 3030)


## Printed circuit board (PCB) components
<!-- maybe add actual photo of assembled pcbs-->
<p align="center">
  <img src="https://github.com/cellworld/robot_assembly/blob/master/images/pcb.png" alt="pcb" width="600" height="300">
</p>

* **Microcontroller** (ESP32-WROOM-32D, Espressif Systems, Shanghia, Shanghai, China)
* **Motor driver** ( DRV8833 Dual Motor Driver Carrier, Pololu, Las Vegas, Nevada, USA, part no. 2130)
* **Voltage regualtor** (IC REG LIN 3.3V 500MA SOT223-4, Texas Instruments, Dallas, TX, USA, Digi-key part no. 296-13424-1-ND)
* **Resistor** $10K \Omega$ (RES SMD 10K OHM 5% 1/10W 0603)
* **Capacitor** $0.1 \mu F$ (0.1 µF ±20% 50V Ceramic Capacitor X7R 0603 (1608 Metric))
* **Push button** (TACT 5.2 X 5.2, 1.5 MM H, 260GF, C&K, Digi-key part no. CKN12221-6-ND)
* **Red LED** (SMD 0603 (1.6mm x 0.8mm) Red LED Diode, Chanzon)
* **Resistor** $1 \Omega$ (RES 1 OHM 5% 1/4W 0402)
* **Drivetrain motor cable** (6 CIRC PICOBLADE RECP:PLUG 150MM, Molex, Lisle, IL, USA, Digi-key part no. 	900-2181130601-ND)
* **Plastic gearmotor cable** (JUMPER WIRE 0.1" 2-PIN 6", SparkFun Electronics, Niwot, CO, USA, Digi-key part no. 1568-1929-ND)
* **PCB connection cable** (JUMPER WIRE 0.1" 5-PIN 6", SparkFun Electronics, Niwot, CO, USA, Digi-key part no. 1568-1932-ND)

## PCB Assembly
This PCB was design using EAGLE. It is PCB CAD software. EAGLE is available from Autodesk either as part of the Fusion 360 software package or you can a free version of just EAGLE [here](https://www.autodesk.com/products/eagle/free-download). The EAGLE project, associated library, and gerber files are located in the pcb directory [here](https://github.com/cellworld/robot_assembly/tree/master/pcb/).



## Chassis assembly
<p align="center">
  <img src="https://github.com/cellworld/robot_assembly/blob/master/images/robot_labeled_assembly-01.png" alt="labeled robot" width="400" height="400">
</p>

### Main chassis
1. Attach the two ABS idler sprockets from the *track set* to *chassis.stl* with a M3 shoulder bolt with a 5mm threaded portion, a washer, and a bolt.
2. Mount two *drivetrain motors*  to *chassis.stl* with M3 screws
3. Attach the two ABS drive sprockets to the *drivetrain motor* shafts
4. Attach the two silicone tracks
5. Insert the *main PCB* into the back of the *chassis.stl* and connect it to the *drivetrain motors*
6. Insert the *battery* and connect it to the *main pcb*
   
### Stimuli module 
1. Insert two M3 standoffs into the two front through holes in *chassis.stl*
2. Press fit the *pump_holder.stl* onto the standoffs
3. Add the *16g CO2 canister and inflator*  with *lever_arm.stl* press fit onto it
4. Slide components into the back channel on the  *pump_holder.stl*:
   1. *motor_platform.stl*, so that its rounded surface rests against the CO2 canister
   2. *plastic gearmotor* (with *cam.stl*  fixed to it with the *motor shaft adapter*)
   3. *motor_stopper.stl* 
5. Fix the PCB with LEDs on it to the top of the *motor_stopper.stl* and connect it to the *main PCB* and the *plastic gearmotor*
   
# Code
Relevant code for the robot resides in separate repositories.
* OTA programming code: [Link](https://github.com/cellworld/ESP32_OTA_programmer)
* Embedded code for BotEvade task: [Link](https://github.com/cellworld/robot_embedded_code/tree/b2fe92d203f52c9526e03de08260bb5708b2de43)

