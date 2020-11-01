# M5StickC Binary Clock

A "Simple" binary clock for the M5StickC.  
Binary Clocks are fun, and can confuse people, but really are pretty simple. Most use dots, or some other display for the bits, this one is a bit different, using the value of the bit as the display. IE: 10100 Which is 20 is displayed as 16 _ 4 _ _ (The _ are just empty spaces).  
The 1st line is hours, the next line is minutes, and last is the seconds.  

To make this work, you just need to add your SSID, and wifi password.  
The ArduinoJson library is also required, you should be able to find that using the library manager.  

once connected to the internet, the sketch attempts to do a best guess of your timezone using the worldtimeapi.org site, it will then set the timezone offset, get the time from a NTP server and set the real time clock of the M5StickC.  
The display is updated using the RTC, once an hour it will attempt to connect to a NTP server and correct the time if needed.  

Please note that I've only tested this in my home timezone (EST with daylight savings), it's not been tested anywhere else, so please let me know if the time is off and maybe we can figure out why! :-)  
It should also be noted that it is a best guess, so if it doesn't have the right time, try to reset and start the sketch again.  

Currently it displays the time in a white font, it is possiable to change to other colors if you don't like white.  I considered making the hours, minutes, and seconds all different colors at one point...then changed my mind.  

I welcome feedback, and collaboration.  

https://youtu.be/Ex9fA5D8e_M  

## Libraries

Because the Arduino IDE has been getting pretty bad handling libraries, I've included the libraries used in the src directory of the sketch. These libraries may have been slightly modified to work from the sketch directory, and do not include the examples.  

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request

## Support Me

If you find this or any of my projects useful or enjoyable please support me.  
Anything I do get goes to buy more parts and make more/better projects.  
https://www.patreon.com/kd8bxp  
https://ko-fi.com/lfmiller  
https://www.paypal.me/KD8BXP  

## Other Projects

https://www.youtube.com/channel/UCP6Vh4hfyJF288MTaRAF36w  
https://kd8bxp.blogspot.com/  


## Credits

Copyright (c) 2019 LeRoy Miller

## License

This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see <http://www.gnu.org/licenses>
