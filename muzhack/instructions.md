**For Rev 2.1 PCB**

# About the BOM

All the parts are relatively straightforward once you have the Eurorack specific sockets and
vertical pots - both available from Thonk. The only tricky and critical part in Europe is the
[vertical SD Card Reader from Yamaichi](http://www.yamaichi.de/?id=301&L=0), which I've only
found available in small numbers from
[Acme in Italy](http://www.acmesystems.it/catalog_sdcard).
This part is available in the US from Mouser as part 945-PJS008U-3000-0.

NB: You will also need:

* [Micro-B USB Cable](https://www.pjrc.com/store/cable_usb_micro_b.html) - a Kindle cable works fine
* MicroSD card, up to 32gb. Teensy developer Paul Stoffregen recommends Sandisk Ultra MicroSD cards

Button colours:

* White 611-D6R00F1LFS
* Grey 611-D6R10F1LFS
* Yellow 611-D6R30F1LFS
* Red 611-D6R40F1LFS
* Green 611-D6R50F1LFS
* Blue 611-D6R60F1LFS
* Black 611-D6R90LFS

# Building the Module

## Populating the boards

![Tops of Rev 1 boards](https://github.com/TomWhitwell/RadioMusic/raw/master/Collateral/BuildImages/48.jpg)
Tops of Rev 1 boards

![Bottoms of Rev 1 boards](https://github.com/TomWhitwell/RadioMusic/raw/master/Collateral/BuildImages/47.jpg)

### Front Board

* The front board is the one with the sockets and pots on it
* The top of the board is the side with the sockets, the bottom of the board has the big logo
* All the components apart from the pin headers go on the top of the board (so you solder on the bottom)
* Start by populating all the resistors and BAT42 diodes
* Make sure the diode orientation matches the PCB silkscreen

![Diodes](https://github.com/TomWhitwell/RadioMusic/raw/master/Collateral/BuildImages/44.jpg)

* If you are using a Rev1 board, fix the grounding problem on R21 and R10 by soldering their legs to R13 at the 'super careful' end. This is already fixed on the red PCBs from Thonk.
  - NB: Red boards from Thonk also say Rev1 (Sorry!).
  - Your board is **fixed** if it has: Curved traces, R11 is 1.5k (not 1k), you can see a trace between the legs of R21, R13, R10. **Fixed** boards do not need this ground bug fix.
  - For more help identifying a Rev1 PCB, [go here](https://github.com/TomWhitwell/RadioMusic/issues/58)

![Grounding problem](https://github.com/TomWhitwell/RadioMusic/raw/master/Collateral/BuildImages/42.jpg)

Fixing the ground bug on the Rev1 boards.

* Do NOT solder the LEDs yet
* Next, add the larger components
  - The SD card has very fine wires, be very slow and patient when placing it and soldering it
  - The pins of the button are quite tight - push it in hard to ensure the white base is flush against the PCB.
  - Make sure the flat edge on the button matches the flat edge on the PCB silkscreen.
  - Metal shaft Alpha pots will give a stronger module than the pots used in this prototype. Remove the locating pins on the front of the pots, if you have them.

![Larger components](https://github.com/TomWhitwell/RadioMusic/raw/master/Collateral/BuildImages/43.jpg)

Adding larger components

![Button base](https://github.com/TomWhitwell/RadioMusic/raw/master/Collateral/BuildImages/41.jpg)

Ensure the button base is flush with the PCB

* Cut the pin headers to fit and solder them to the bottom of the board. The wonky holes are deliberate - they hold the pins in place while you're soldering.

![Pin headers](https://github.com/TomWhitwell/RadioMusic/raw/master/Collateral/BuildImages/40.jpg)

* Now attach the LEDs

  - Put the LEDs into place. Be very careful to get them the right way around. The longer leg goes into the hole marked with a cross.
  - Before soldering the legs, put the front panel on. Finger tighten the nuts on the sockets and pots
  - Put the LEDs into place pointing through the holes in the front panel, and carefully solder them into place.

![LEDS](https://github.com/TomWhitwell/RadioMusic/raw/master/Collateral/BuildImages/38.jpg)
![LEDS](https://github.com/TomWhitwell/RadioMusic/raw/master/Collateral/BuildImages/37.jpg)
![LEDS](https://github.com/TomWhitwell/RadioMusic/raw/master/Collateral/BuildImages/36.jpg)

Congratulations. You're half way there.

### Back Board

* The back board is the one with the Teensy and the power header on it
* The top of the board is the ferrite beads and the TL074 IC. The bottom of the board has a logo, the Teensy and the power connector.
* Install the ferrites, resistors and diodes first, being careful to get the diodes the right way around. The big black 1N4001 diodes go at the top of the board in the power supply section. The little glass BAT42 diodes are behind the Teensy at the bottom.

![Back board](https://github.com/TomWhitwell/RadioMusic/raw/master/Collateral/BuildImages/35.jpg)

* Capacitors next. Don't confuse the 1n (1000pf / 102) with the 100n (0.1uf / 104). There are two kind of 100n capacitor; the box-shaped poly caps go in the audio path, the cheap ceramics are used in the power supply. The electrolytic 10Uf capacitors need to be the right way round - the short wire goes into the hole marked -.

![Capacitors](https://github.com/TomWhitwell/RadioMusic/raw/master/Collateral/BuildImages/34.jpg)

* NB: The Rev1 PCB silkscreen for the 78L05 regulator is WRONG - solder it in the other way around. Note on the Rev2 Thonk Red PCBs the regulator silkscreen is fixed and correct. If you can't find the 78L05 in the Thonk kit... it's pressed into the foam in the silver ESD packet.

![Power Regulator Fix](https://github.com/TomWhitwell/RadioMusic/raw/master/Collateral/BuildImages/31.jpg)

Rev1 board Power Regulator Fix

* Add the IC socket, fuses and, on the back, the Power header and trimmer

![IC socket](https://github.com/TomWhitwell/RadioMusic/raw/master/Collateral/BuildImages/32.jpg)
![IC socket](https://github.com/TomWhitwell/RadioMusic/raw/master/Collateral/BuildImages/33.jpg)

* Finally, add the female socket to the FRONT of the board

  - Place the female socket onto the front PCB and cut to fit both sides
  - Put the two boards together - you may have to fold the fuses in a little to fit
  - Solder the female sockets onto the back board

![Female socket](https://github.com/TomWhitwell/RadioMusic/raw/master/Collateral/BuildImages/12.jpg)
![Female socket](https://github.com/TomWhitwell/RadioMusic/raw/master/Collateral/BuildImages/11.jpg)
![Female socket](https://github.com/TomWhitwell/RadioMusic/raw/master/Collateral/BuildImages/09.jpg)
![Female socket](https://github.com/TomWhitwell/RadioMusic/raw/master/Collateral/BuildImages/08.jpg)

Congratulations. You're nearly done.

## Mounting the Teensy

**Remember to prepare the teensy first before soldering or mounting**

Read here - [Preparing the Teensy 3.1 for Radio Music](https://github.com/TomWhitwell/RadioMusic/wiki/Preparing-the-Teensy-3.1)

* There are two ways to mount the Teensy:

  - The neatest and most secure is to solder it directly to the module.. however we only recommend
  this if you are very confident about your soldering! If you are not as confident then use
  female headers so the teensy can be easily removed to troubleshoot (see below).
  ![Female headers](https://github.com/TomWhitwell/RadioMusic/raw/master/Collateral/BuildImages/19.jpg)
  - But if you're worried about mounting a £20 module permanently, you can use female pin
  sockets to make a socket for the Teensy. Build the socket on the Teensy, then solder it
  into place on the module. Remove the Teensy before testing the module - be careful not
  to bend any pins.
  ![Female pin sockets](https://github.com/TomWhitwell/RadioMusic/raw/master/Collateral/BuildImages/18.jpg)
  ![Female pin sockets](https://github.com/TomWhitwell/RadioMusic/raw/master/Collateral/BuildImages/14.jpg)
  ![Female pin sockets](https://github.com/TomWhitwell/RadioMusic/raw/master/Collateral/BuildImages/15.jpg)
* Always remove the Teensy before performing desoldering or rework on the PCBs!
