# Arribada Penguin Monitoring Platform

Arribada Penguin Monitoring Platform is a standalone device featuring a Raspberry Pi and a Raspberry Pi Camera Module. These user-instructions define the use-case of the device and serve as the guideline for development and creating the software support requirements.

<img
src="/pics/IMG_20180122_102543_01.jpg"  width="500px" height="375px">


Device consists of:
 * Camera unit:
    * Raspberry Pi Zero W
    * Raspberry Pi Camera Module V2
    * Samsung EVO Plus 64GB microSD card
    * Pira Zero V3
    * 6x 18650 LiPo Cell 2900mAh/4.2V
    * Nanuk NANO 330 waterproof enclosure
    * Multi-directional camera mount
 * Solar power:
    * 2x Voltaic Systems 6V 6W solar panel
    * 2x Voltaic Systems solar panel extension cable
    * Multi-directional solar panel mount
 * Accessories
    * Allen-key tool for mounting
    * SD to microSD adapter
 * Additionally required and not included
    * Pole (round or square) up to 50mm in diameter
    * Metric wrench size 13
    * Compass and tilt measuring device for pointing the solar panels


## Key user features
 * Captures photos and videos in Full HD resolution
 * Configurable time-interval
 * Autonomous operation for 356 days with no charge
 * Adaptive adjustment of capture cycle if extra power is available


## Primary use-case scenario
 * Charge the device from mains power via microUSB connection (up to 24h with 1A 5V USB charger)
 * Configure the preferred capture cycle based on the date for example:
   * month / morning / evening / interval
     * January / sunrise / sunset / 1h
     * February / 05:00 / 18:00 / 30min
     * March / sunrise / 15:00 / 2h
     * April / 12:00 / 13:00 / 1min `unit does not sleep in this case`
 * Deploy the device on-site
   * Connect solar panels
   * Turn the power switch on
   * Turn the debug switch on
   * Unit is on and WiFi appears
     * Recent image seen on web
   * Turn debug switch off, unit then operates normally
 * Unit or microSD card is retrieved/replaced
   * Connect the SD card to Windows and copy images
   * Change or modify the capture cycle or other parameters in config file


## Mounting

The Arribada Penguin Monitoring Platform features:
* NANUK camera case
* solar panels
* 2 mounts with clamp jaws and screws

<span><img
src="/pics/IMG_20180122_100336.jpg"  width="400px" height="300px">
<img
src="/pics/IMG_20180122_095626.jpg"  width="400px" height="300px"></span>


To mount the APMP to pole, first take mount, clamp jaws and screws. Insert the four screws through the holes of the mount and the first two clamp jaws.

<span><img
src="/pics/IMG_20180122_100502.jpg"  width="400px" height="300px">
<img
src="/pics/IMG_20180122_100640.jpg"  width="400px" height="300px"></span>


Attach the mount on the pole using the other two clamp jaws, spring washers and nuts. Tighten the nuts using a 13mm wrench.

<span><img
src="/pics/IMG_20180122_100918.jpg"  width="400px" height="300px">
<img
src="/pics/IMG_20180122_100959.jpg"  width="400px" height="300px"></span>


Attach the other mount using the other set of clamp jaws, spring washers and nuts. 

<img
src="/pics/IMG_20180122_101352.jpg"  width="400px" height="300px">


Attach the NANUK camera case and solar panels and secure it with screws on the camera case and solar panels as seen in the picture.

<img
src="/pics/IMG_20180122_101625.jpg"  width="400px" height="300px">

<span><img
src="/pics/IMG_20180122_101707.jpg"  width="400px" height="300px">
<img
src="/pics/IMG_20180122_101738.jpg"  width="400px" height="300px"></span>


Set the desired angle for the NANUK camera case and solar panels and secure it in place with two screws on each mount as seen in the picture.

<span><img
src="/pics/IMG_20180122_102104.jpg"  width="400px" height="300px">
<img
src="/pics/IMG_20180122_102009.jpg"  width="400px" height="300px"></span>


Connect the solar panels to the camera case. Use the supplied extension cables if necessary.

<img
src="/pics/IMG_20180122_102318.jpg"  width="400px" height="300px">
