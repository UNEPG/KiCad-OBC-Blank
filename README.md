# KiCad-OBC-Blank
Starter files for https://github.com/UNEPG/KiCad-OBC

## Working with the Files

1. Download the repository from GitHub.

2. Unzip the files to the desktop.

3. Double click to open the KiCad Project

4. As previous modules had already introduced KiCad and it's essential tools, we are not going to repeat the same process, instead, we are going to focus on creating the PCB using existing component libraries.

5. We have already provided the main components that are going to be utilized in this project, and they are the **Raspberry Pi** MPU, **HTS221** humidity and temperature sensor, **LPS25H** pressure sensor **SDS011** PM2.5 dust sensor. we also included some **capacitors**, **mounting holes** and **power symbols** to use.  (components should be highlighted in the video with rectangle areas)

6. Let's utilize the Raspberry Pi MPU first.  (End of first video here)

7. [PPT] We need 5V, 3.3V power supply, Ground, I2C and UART lines from the raspberry Pi. 

8. [VIDEO2 - RPI] Let's create global labels on all the pins we needed. we will start from the 3.3V and 5V, then the I2C and UART, and then the Ground Pins. All the GND pins from the MPU should be connected to the ground. At the end remember to add 'no-connection-flag' to the pins that we are not using.

9. [Documentation Scrolling Video(3)] HTS221 is a humidity and temperature sensor, requires 1.7 to 3.6 volt power supply and communicates with the host device using either SPI or the I2C interface. 

10. [Video4] Lets connect pin1 to the 3.3v (Global Label) and pin 5 to the ground. Documentation of the sensor recommends a 100 Nano-farad capacitor between the power and the ground, so let's do that . We also connect the SDA and SCL pins from the raspberry pi to the sensor. Pin6 used to enable the I2C interface and let's connect that to the 3.3v too. Add 'no-connection-flag' to the pin3, as we are not using that pin.

11. [Video5] And we will continue the same process for another sensor. 

    1. First we will connect the  the pin 10, pin 1 and pin 6 to the 3.3 volt.  (Using Global Label)
    2. and let's also add several decoupling capacitors between the ground and power to filter the noise. 
    5. Lets also connect the I2C lines from the raspberry pi to the sensor. 
    8. Connect the Pin3,8, and 9  to the ground
    8. also connect pin 5 to the ground.
    9. Add no-conection flag to all the other pins which we are not using in this project. 
    9. Now lets connect the SDS011 Dust sensor. Add the power and ground, then connect Tx from the raspberry pi to the RX of the SDS011, and connect the Raspberry Pi Rx pin to the TX, add 'no-connection-flag' to all other pins.
    10. Also, let's connect the power connector. It's also a  common standard to connect the mounting holes to the ground.

12. [Video6] 

    1. We will annotate the schematics, keep everything as default. 
    2. Let's assign foot prints for our components. 
    3. Open the PCB editor, update the PCB from schematics and select the 'Edge Cuts' layer and create a rectangle PCB shape.
    4. and move the component's position to the proper locations (it dose not have to be the same place as it's shown in the video, you can place them anywhere in the rectangle area). 
    5. We also want to rotate the SDS011 sensor so that the pins will be closer to the raspberry pi. You might need to re-arrange the mounting holes. 
    6. you can turn off the ‘silks screen’ layer or remove the text to the ‘F.Fab’ layer if you want.
    7. Now wire all the connections between RPi and the sensors one by one. Start from UART pins, and then the I2C lines, then connect all the power and ground pins. It's the same process that you've already tried whiling connecting the wires on Fritzing, just be patient and connect them all one by one.
    8. You can assign 3D models for the footprints if you want, I will assign 3D to the Raspberry, and the sensors. I've already prepared all the 3D models for you and saved inside the "Parts" folder. 
    9. In some cases, you also need to adjust the orientation of the 3D model.
    10. Let's see the result in 3D view. 
    11. By doing so, you have already created your first PCB in KiCad.
    
    
    
    
