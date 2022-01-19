# W48-GSM
This project modifies a german telephone of the 1950's, made of bakelit, to a full functional GSM mobile phone.
It can't be distinguished from a genuine phone (in fact, it is an original from ebay), except there is a small switch 
and USB charge connector (and of course, the cable is missing).
Even the dialtone is that one of the 50's, which has been changed in 1978 by german telekom to a continuous tone.
To dial a number, just grab the headphone and dial. It works fine as it did 70 years ago.

Whats inside:
It contains an ESP32. GSM connection is done with the usual SIM800L breakout, just add a SIM card.
The ESP32 decodes the dialed number of the dialplate and it checks the hook contact and the button.
Microfone and speaker are left unchanged and they work great.
It is powered using a 18650 cell which lasts longer than 12 hours (I expect 100 hours after a firmware optimization, still on my todo-list).
To charge, a USB charge controller is included. Of course, it has a USB-C connector.
At phone networks, the bell is usually powered with 60V 25Hz, so I used a boostconverter and a full H-bridge (actually a A4988 
stepper motor driver) to drive the bell with 30V AC, which obviously works very well and sounds delicious.
The button makes no sense for todays phone networks, I abused it to add "redial", "quick dial" and "call back" functionality.
As there was some space left on the PCB, I added a microSD reader and a I2S audio breakout (and a relay to switch audio signals). 
So we have a mp3 player here, too. One may catch some special phonenumbers in firmware which can do all stuff you may imagine: 
play an audio file, automatic fake calls or whatever you want. Bluetooth/WiFi is not used in current firmware, I had no ideas what to do with it.
Remote control of the W48 using a smartphone was not a goal for me.

I did several revisions of the PCB to achieve an easy to make project for everyone.
If you want to make your own item, here is your todo list:
- buy a "W48" on ebay (available in white bakelit, too), this may cost between 15 and 50 EUR.
- order a PCB by sending the gerber-files contained in the project to a PCB manufacturer like JLCPCB or PCBWAY. (or mail me, I have some PCBs left)
- order the items of the BOM list from aliexpress, which may cost 40 EUR
- solder that stuff to the PCB (SMD soldering requires a few easy-to-solder 0805 parts only)
- download firmware to ESP32, using arduino IDE or something similar. (I use Visual Studio Community Edition and the visualMicro extension which costs a bit)
- crimp suitable connectors to dialplate, button, hook and headset, this is the hardest part
- insert 18650 cell and a SIM card (PIN must be disabled)
- switch on and have fun with your brand new retro mobile.
- maybe you want to add some mp3 tracks to a microSD card for further fun
- maybe you have lots of ideas how to pimp functions of the toy.KiCad schematics and sourcecode are included.

If something does not work well or is not clear, do not hesitate to mail me.

