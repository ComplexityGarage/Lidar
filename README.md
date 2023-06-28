# Lidar-based obstacle detector
# Authors 
- Monika Rasz
- Piotr Słowik
# Description of the project 
A simple system that scans the environment, presents real-time distance from obstacles on a graph and beeps if an object is too close.
# Science and tech used 
## Principle of operation
The lidar sensor uses a class 1 laser and a detector sensitive to its wavelength to calculate the TOF (time of flight - the time between sending a laser impulse and detecting the light reflected from an obstacle), which is then used to calculate the distance. 

By placing the sensor on the servomechanism, we can obtain a real-time depth image in a half-plane at the frequency of around 1Hz.
## Elements used in the project
### Raspberry Pi (4, model B, 2018)
https://www.raspberrypi.com/products/raspberry-pi-4-model-b/
### Lidar distance sensor (TF Luna 8m UARTI2C)
https://botland.com.pl/czujniki-time-of-flight/16638-laserowy-czujnik-odleglosci-lidar-tf-luna-8m-uarti2c-5903351249041.html
### Servo (FEETECH Standard Servo FS5103B)
https://www.pololu.com/product/3424  
Servo has a running angle of approximately 180°, the angular velocity can be easily modified in a wide range.
### Piezo buzzer, 5V power generator, a breadboard and quite a lot of wires
# State of the art 
## Software
For configuration and control of the lidar sensor, we followed the tutorial available at https://makersportal.com/blog/distance-detection-with-the-tf-luna-lidar-and-raspberry-pi and used the software mentioned in it (https://github.com/makerportal/tfluna-python), which we later modified to accommodate the use of servo and piezo buzzer. The final code is in the file Lidar_test_rt.py.
## The circuit

# What next?
- The servomechanism does not work very smoothly, even with no load on the top. It is particularly noticeable when the servo is controlled by the same piece of code (same loop) as the lidar sensor. We couldn't identify the cause of the jittering, even though we tested various power sources. This is the first step towards an overall improvement of the performance of the system and further development, as too much jittering impedes the imaging process.
- Designing a dedicated camera holder for a more secure fit.
- Creating a 2D (or 3D) image of the surroundings.
# Sources 
- [Writing on GitHub] ( https://docs.github.com/en/get-started/writing-on-github ) 
