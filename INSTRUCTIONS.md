# Arribada PMP
# Instructions

## Description of operation
When the device is turned on and running, it will periodically enable and disable 5V power supply for Raspberry Pi module.
After enabling the 5V power supply, Raspberry Pi module will turn on, take a picture with Raspberry Pi camera, save it to USB flash drive and then shut itself down. With shutdown Raspberry Pi also signals the main board that it can now disable the 5V supply.
Main board will wait specified amount of time before again turning on the Raspberry Pi which will repeat the cycle.

## Turning on the device
1. Insert batteries into the device. Beware of the correct battery polarity; follow the markings on plastic battery holders.
2. To start the device, click the “battery activate” button in the corner of the board. You will be greeted with the IRNAS logo and Arribada PMP text, which will appear on the OLED display.
3. After the initial boot message on the OLED screen the device should be working normally.

## Checking captured pictures and setting environment variables
To access the captured pictures and to change the settings, user will have to remove the USB flash drive, which is connected to the Raspberry Pi. Two storage places are interesting for the end user, the “camera” directory and the “environment” file.
Captured pictures can be accessed in the “camera” directory. The pictures are named like this: `snapshot-{year}-{month}-{day}--{hour}-{minute}-{second}--{light}-(voltage)-(temperature).jpg`. Light parameter corresponds to light level detected by sensor when taking the photo.
System can be configured by changing the environment variables in the “environment” file, located in the main directory. File can be opened and modified with a text editor, e.g. Notepad or Notepad++.
User can set how long will the Raspberry Pi stay turned off before being turned on to make a photo, which defines the time-lapse interval. This can be set by changing the values of “PIRA_SLEEP” and “PIRA_WAKEUP” variables, which take time values in seconds. Both variables should have the same value. For example, if we want the Raspberry Pi to stay off for 5 minutes before turning it on again, we will set the “PIRA_SLEEP” and “PIRA_WAKEUP” variables both to 300:
*	PIRA_SLEEP="300"
*	PIRA_WAKEUP="300"
In normal operating conditions, Raspberry Pi is turned on for about 40 seconds. This means that setting the variables to 300 will set the time-lapse interval to approx. 340 seconds.
⚠️ ATTENTION! Do not change any other variables to avoid disrupting the operation of the device!

## Accessing the device information on OLED display
Some basic information about the device can be seen on the OLED display. User can see the “current time (UTC)”, “number of captured photos” and” time to next wakeup”. The information is displayed by pressing either “Button 1” or “Button 2” on the side of the board for approx. 5 second.
The current time (UTC) is obtained through the GPS. If there has yet been no GPS fix after the device lost and regained power, a reset date that is saved in memory will be shown, which is 1.1.2020, 00:00.
Number of captured photos and time to next wakeup are obtained from the Raspberry Pi just before the end of each cycle. If no cycle has yet been performed after the device lost and regained power, this information will not be available.
