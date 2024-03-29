bluepy
======

Python interface to Bluetooth LE on Linux

This is a project to provide an API to allow access to Bluetooth Low Energy devices
from Python. At present it runs on Linux only; I've mostly developed it using a
Raspberry Pi, but it will also run on x86 Debian Linux.

There is also code which uses this to talk to a TI SensorTag (www.ti.com/sensortag).

This is beta-quality code, not all LE functions are implemented.

Installation
------------

The code needs an executable 'bluepy-helper' to be compiled from C source. You can
do this by running 'make' in the bluepy/ subdirectory. Currently the Makefile is
configured to build for ARM Linux; you will need to set the ARCH variable in it 
appropriately for other platforms.

The sources need glib and dbus headers to compile. On the Pi you can get these with:
  sudo apt-get install libglib2.0-dev libdbus-1-dev

There are general instructions for setting up BlueZ on the Raspberry Pi at:
  http://www.elinux.org/RPi_Bluetooth_LE
  
Once 'bluepy-helper' is built, you can copy it and the two .py files to somewhere
convenient on your Python path (e.g. /usr/local/lib/python2.7/site-packages/).

License
-------

This project uses code from the bluez project, which is available under the GPL.

The Python files are released into the public domain by their author, Ian Harvey.

Update Notes
-------------

Fix for no flush. File:btle.py, line 161 added flush() 
Fix for no encode. File:btle.py, line 299 added str.encode




