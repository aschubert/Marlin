# Marlin 3D Printer Firmware

This is my attempt to build a auto calibrating and auto bed leveling firmware for the Dreammaker Overlord Pro based on https://github.com/RichCattell/Marlin but with Ultimaker like menu system and other features available in the original Dreammaker Firmware (https://github.com/jimaobian/MarlinForOverlord).

## Progress so far

* Printing over USB works, nothing else (no UI, no SD-Card, ...)
* Calibration using a z-probe works
* Bed-leveling using a z-probe works

## How to build

I do the development for this on Mac OS X, so these instructions focus on this environment. It should be easyly adaptable to other Unix environments like Linux, unfortunately not so easy to Windows.

Building using the Arduino IDE is not recommended and not tested. I'm a command line guy so I prefer to use make.

You need to have Ardunio IDE 1.0.5 installed, as it contains avr-gcc and avrdude which are used to compile and upload the firmware.

So edit Makefile, basically the ARDUINO_INSTALL_DIR, AVR_TOOLS_PATH and UPLOAD_PORT to match your environment. Then it is simply a matter of:

```sh 
make
make upload
```

## Future plans

* Try to port this back to recent Marlin
