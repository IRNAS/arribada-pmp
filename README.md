# Arribada Penguin Monitoring Platform - v2 - development

Arribada Penguin Monitoring Platform (APMP) is a standalone device featuring a Raspberry Pi and a Raspberry Pi Camera Module with a number of additonal features. The below image is of previous version to form the list of necessary changes.

<img src="/pics/apmp.png"  width="850px">


## Key user features - v2
* Capture image/video at defined intervals
* Report system status/sensors via Lora (optional)
* Report system status/sensors via RockBlock Iridium (optional)
* Optional sensors:
  * Ultrasonic distance
  * Temperatures
  * GPS - location
* Power:
  * Batteries
  * Solar charging
* USB flash drive - user removable - contains all images and other captured data
  * contains images/videos
  * contains json with settings
* SD card with OS is read-only and not to be removed
* on/off switch
* 2x push button
  * button 1: test mode - push to turn on the system for 10 minutes
  * button 2: general purpose
* Test mode:
  * WiFi enabled, user can connect and check camera image or download all images
  * Each time test mode is enabled an image is taken.
* Bluetooth:
  * System status printout
  * Enable test mode
  * Configure settings
* Lora:
  * Enable test mode 
  * Configure settings
  * LacunaSpace communication
 
## Key user stories - v2
1. Penguin camera - Install on a pole in Antarctica. Arrive at location and turn on. Push button for test mode. See images via WiFi on smartphone or leave running and remove USB. To check camera alignment and correct operation. Leave device running for year or more, come pack and swap USB flash drive. Meanwhile real-time reporting via Lora or Lacuna, each day.
1. River camera - Install above a river with ultrasonic sensor and optional rockblock connection. Once above river enable the test mode via bluetooth. Check via WiFi the alignment and operation. Leave running and get real time sensor data. retrieve in a year to get back the photos.
1. TBD

## Configurable parameters - settings - v2
All the setings are defined as Environmental vairables in Linux, settings are changed using one of the following methods: json file present on the USB flash drive, system auto-updates values from it, via lora or via Balena if used

* User definable parameters:
 * capture schedule per month:
   * start time (UTC) - daily - fixed hour or `sunrise` (default 0:00)
   * end time (UTC) - daily - fixed hour or `sunset`(default 23:59)
   * interval (in minutes) - 0 to 24*60 (default 60)
 * location (automatic if GPS present):
   * lat (used for sunrise/sunset calculation)
   * lon (used for sunrise/sunset calculation)
 * capture type:
   * image
    * flash config
   * video
 * pira variables:
   * all timer values and defaults
   * lora parameters
   * rockblock parameters
   * sensor reporting interval
 * battery settings:
   * empty: default 10% - do not wake up the RPi below that
   * low-battery: default 30% - wake up only once a day
   * normal: general operation

## Specification

Device consists of:
 * Camera unit:
    * Raspberry Pi Zero W
    * Raspberry Pi Camera Module V2
    * Sandisk 16GB microSD card
    * Pira Smart V2 integrated board with battery mounts
    * 6x 18650 LiPo Cell 2900mAh/4.2V
    * Nanuk NANO 330 waterproof enclosure
    * I2C display for status
    * 2x user button
 * Optional:
    * Flash
    * Lora antenna
    * Rockblock Iridium or Lacuna module
    * Ultrasonic sensor
    * Thermometer
 * Solar power:
    * 2x Voltaic Systems 6V 6W solar panel
    * 2x Voltaic Systems solar panel extension cable
    * Multi-directional solar panel mount
 * Accessories
    * Allen-key tool for mounting
    * SD to microSD adapter
 * Mounting:
   * Simple strap mount (default)
   * Advanced KORUZA mount (optional)
 * Additionally required and not included
    * Pole (round or square) up to 50mm in diameter
    * Metric wrench size 13
    * Compass and tilt measuring device for pointing the solar panels
    
 ## Key desing considerations
 * Battery protection consider LC05111CMT for every 2 cells in parallel
 * Consider battery low temperature charge cutoor toprotect cells in winter
 

