# Volvo MELBUS

## Bluetooth and custom text in the display

N.B. If you do not use D2 for the clock pin, you MUST change it to pin D3, and change INT_NUM to 1. 

### This is my latest code and schematics. If anyone misses the old files, tell me and I'll put them up again.
But I think this is so much better than earlier versions so I deleted them.


Parts list:
* Arduino Nano 5V
* Transistor that can handle more than 0,5A
* Resistors:
   * 3x 100Ω
   * 1x 1KΩ
* A rectifier diode (> 0,5A e.g. 1N4004)
* 1x 470 uF capacitor
* Cables and optionally some connectors for fast removal of device from the car. (not included in schematics)
* Male DIN plug, 8 pin, 270 degrees
* CSR8645 Bluetooth device with 12v regulator onboard
* 4066 bilateral switch IC (optional to remote control audio source)
* Ground loop isolator (yes, there is no way around it if you want to get noise free sound)

Some knowledge of electronics, and you need to be good at soldering. You are responsible if things break! Not me! 

Credits to 
* [Karl Hagström](http://gizmosnack.blogspot.se/2015/11/aux-in-volvo-hu-xxxx-radio.html)
* http://volvo.wot.lv/wiki/doku.php?id=melbus.
* Vincent

This project shows the way I did it. I'm a hobbyist, not a professional electronics engineer. Proceed at your own risk. The devices use different voltage levels, so there is a chance that you will let the magic smoke out. (Hence the 4066)

Demo https://youtu.be/jGOKGUjlLhI

## Schematics
![schematics](schematics/8645_4066.png)
Found an error: R1 should be connected to the right of the diode.
