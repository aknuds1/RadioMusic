##Module Hardware Test file  

[![](https://i.vimeocdn.com/video/503708029.webp?mw=600&q=70)](https://vimeo.com/117123053)  
[CLICK TO WATCH THE VIDEO](https://vimeo.com/117123053)  

ModuleTest.ino is a quick way to check that the hardware in your module is working correctly.  

If you cut the power trace, you'll need both +/-12v ribbon cable power and USB power to make it work.  

You'll need to install the full [Teensyduino environment](http://www.pjrc.com/teensy/td_download.html). Once that is installed and working (i.e. you can install Blink and see expected results) download and run the [Module Test Sketch](https://github.com/TomWhitwell/RadioMusic/tree/master/Collateral/ModuleTest).  
- You'll see all five LEDs flash in sequence   
- While they're flashing, the module will generate audio - various sine wave tones    
- Once the startup routine is finished, the 4 LEDs are linked to 2xknobs and 2xCV inputs  
- If you run the serial monitor in Arduino, you'll see the knob / CV input values as 0-1024. 
    - Expect to see some jitter from noise - maybe jumping up and down 10 points (these numbers are smoothed by the firmware later on), but you should be able to move each pot from 0 - 1024 smoothly.  