---
layout: post
title:  "Mixtape Board"
date:   2017-02-05 11:57:45 -0800
categories: hardware_projects
---
# Mixtape Board

(Oct. 2016 - Dec. 2016)

This board is a digital "mixtape," designed to be a compact way to share a music playlist and recordings with friends.

Similar to a cassette, when given to others it has a surprise factor of not knowing what's up next.

Board was built up in December 2016, and general functionality (power regulation, bluetooth control, SD card, audio out) was confirmed.
<br>
### Main Features:
* Plug-in bluetooth module (like the [HC-06](http://www.gearbest.com/sensors/pp_241478.html) or [CC2540](https://tronixlabs.com.au/breakout-boards/bluetooth/cc2540-serial-bluetooth-v4-0-ble-module-ibeacon-australia/)) allows for remote control with an phone or computer.
* Power comes from a rechargeable [18650 Li-ion battery.](https://github.com/bkeegs/18650-Charge-Board)
* Teensy 3.2 is used as the microcontroller.
* Audio is single channel, 3W Class-D amplifier using a PAM8009DHR
<br>
### Schematic:
![Schematic]({{ site.url }}/assets/images/mixtape_sch.PNG)
<br>
### PCB Top:
![Schematic]({{ site.url }}/assets/images/mixtape_board1.PNG)
<br>
### PCB Bottom:
![Schematic]({{ site.url }}/assets/images/mixtape_board2.PNG)
<br>
### Built Board:
(add picture here)

<br><br>
[Github page](https://github.com/bkeegs/18650-Charge-Board)
<br>
Ordered from [oshpark here.](https://oshpark.com/shared_projects/jIOHaPzt)
