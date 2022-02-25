# KiCad-OBC-Blank
Starter files for https://github.com/UNEPG/fritzing-obc

## Working with the Files

1. Download the repository from GitHub.

2. Unzip the files to the desktop.

3. Double click to open the KiCad Project

4. As previous modules had already introduced KiCad and it's essential tools, we are not going to repeat the same process, instead, we are going to focus on creating the PCB using existing component libraries.

5. We have already provided the main components that are going to be utilized in this project, and they are the Raspberry Pi MPU, HTS221 humidity and temperature sensor, LSM9DS1 9-axis accelerometer, gyroscope and magnetometer. we also included some capacitors, resistors and power symbols to use.  (components should be highlighted in the video with rectangle areas)

6. Let's utilize the Raspberry Pi MPU first.  (End of first video here)

7. [PPT] We need 3.3V power supply, Ground and I2C lines from the raspberry Pi. 

8. [VIDEO2] Let's create global labels on all the pins we needed. we will start from the 3.3V, then the I2C, and then the Ground Pins. All the GND pins from the MPU should be connected to the ground.

9. [Documentation Scrolling Video(3)] HTS221 is a humidity and temperature sensor, requires 1.7 to 3.6 volt power supply and communicates with the host device using either SPI or the I2C interface. 

10. [Video4] Lets connect pin1 to the 3.3v and pin 5 to the ground. Documentation of the sensor recommends a 100 Nano-farad capacitor between the power and the ground. We also connect the SDA and SCL pins from the raspberry pi to the sensor. Pin6 used to enable the I2C interface and let's connect that to the 3.3v too. Add 'no-connection-flag' to the pin3, as we are not using that pin.

11. [Video5] And we will continue the same process for another sensor. 

    1. First we will connect the  the pin 23 and pin 1 to the 3.3 volt.  
    2. and let's also add several decoupling capacitors between the ground and power to filter the noise. 
    3. We also add one 10k Ohm pull up resistor to the pin 13. 
    4.  Pin7 and Pin8 is used for enabling the magnetometer and gyroscope, we need to connect them to the 3.3 volt. 
    5. Lets also connect the I2C lines from the raspberry pi to the sensor. 
    6. We are only using I2C for communication, so we will disable SPI through connecting Pin5 and Pin 6 to the ground.
    7. Pin 21 and Pin 24 should be connected to capacitor and ground in serial. The documentation requires 10 nano farad for pin 21 and 100 nano farad for pin 24.
    8. Connect the reset and GND pins to the ground.
    9. Add no-conection flag to all the other pins which we are not using in this project. 

12. [Video6] 

    1. We will annotate the schematics, keep everything as default. 
    2. Let's assign foot prints for our components. 
    3. Then we will generate net list file for the current PCB. 
    4. Open the PCB editor, and we will create a rectangle PCB shape.
    5. Fill both sides of the PCB as ground.
    6.  then import the netlist. 
    7. and move the component's position to the proper locations. 
    8. Now wire all the connections between RPi and the sensors, we will use 'Via' to for the connections and it makes it much more easier.
    9. You can assign 3D for the footprints if you want, I will assign 3D to the Raspberry, and the sensors.
    10. Let's see the result in 3D view. 
    11. By doing so, you have already created your first PCB in KiCad.

    

    
