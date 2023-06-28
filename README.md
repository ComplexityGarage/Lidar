# Lidar-based obstacle detector
# Authors 
- Monika Rasz
- Piotr Słowik
# Description of the project 
A simple system that scans the environment, presents real-time distance from obstacles on a graph and beeps if an object is too close.
# Science and tech used 
## Principle of operation

## Elements used in the project
### Raspberry Pi (4, model B, 2018)
### Lidar distance sensor (TF Luna 8m UARTI2C)
https://botland.com.pl/czujniki-time-of-flight/16638-laserowy-czujnik-odleglosci-lidar-tf-luna-8m-uarti2c-5903351249041.html
The lidar sensor uses a class 1laser to calculate the TOF 
### servo (FEETECH Standard Servo FS5103B)
https://www.pololu.com/product/3424
### piezo buzzer
Text & plots here... 
# State of the art 
Text & plots here... 
# What next?
- The servomechanism does not work very smoothly, even with no load on the top. It is particularly noticeable when the servo is controlled by the same piece of code (same loop) as the lidar sensor. We couldn't identify the cause of the jittering, even though we tested various power sources. This is the first step towards an overall improvement of the performance of the system and further development, as too much jittering impedes the imaging process.
- Designing a dedicated camera holder for a more secure fit.
- Creating a 2D (or 3D) image of the surroundings.
# Sources 
- [Writing on GitHub] ( https://docs.github.com/en/get-started/writing-on-github ) 
