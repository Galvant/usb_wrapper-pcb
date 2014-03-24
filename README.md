USB Wrapper
===========

This repository contains the KiCAD PCB project files for the USB wrapper project
by Galvant Industries.

This project is entirely open source hardware.

Pre-assembled boards now available at http://galvant.ca/shop/usb-wrapper/

About
-----

Have you ever wanted to charge your smartphone by using your computer, but you
didn't want all of your sync software to load? Maybe you want to use a friend's
computer but you don't really want Windows to start trying to install drivers 
and for your device to open in USB transfer mode. Or maybe the power source is 
simply untrusted and you want to avoid a potential attack.

Inspired by the USB Condom, the USB Wrapper helps with the above by severing 
the USB data lines and only allowing the 
power lines to connect through. This ensures that no data information can be 
transfered between the power source and your device. This helps against known 
attacks such as juice jacking:
http://krebsonsecurity.com/2011/08/beware-of-juice-jacking/

This however does present a problem. In legitimate USB chargers, the data lines
are used to communicate to your device how much power they are capable of
sourcing. The exact means by which they do vary between manufacturers. The 
standard calls for the D+ and D- lines to be shorted together, while companies 
like Apple will apply specific voltages on both lines depending on the charger.
By entirely disconnecting these data lines, your device does not know any 
information about the charger, and will thus assume it is a standard USB2.0
port. This limits means the device will self-limit the charging rate to 2.5W,
even if the charger can in fact handle more.

To deal with this, the USB Wrapper has two slider switches allowing you to tell
your device what kind of charger it is connected to. This also allows you to
mix and match chargers and device manufacturers which don't follow the same 
signalling rules. For example, an iPhone with a Samsung charger cube.

Features
--------

 - Disconnects USB data lines between the host and device, preventing attacks
   such as "juice jacking" and keeps trusted computers from trying to sync
 - Slider switches which allow you to tell your device what kind of charger 
   is connected. Select from dedicated charger port, Sony, open circuit, and
   four different Apple chargers; 500mA, 1A, 2.1A, and 2.5A.
 - USB-B and USB-micro-B connectors on the power side
 - USB-A on the device side
 
License
-------

This work is released under the Creative Commons Attribution-Sharealike 3.0 
license. See http://creativecommons.org/licenses/by-sa/3.0/ or the included 
license/LICENSE.TXT file for more information.
