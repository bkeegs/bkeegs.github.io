---
layout: post
title:  "Chiptune Teensy"
date:   2017-02-07 11:31:45 -0800
categories: hardware_projects
---

(Youtube video to be uploaded here)

This hack was designed as a minimal chiptune player for 3 voices using just a Teensy 3.2 and 3 piezoelectric buzzers.

It uses vishnubob's [python-midi](https://github.com/vishnubob/python-midi) library to parse midi files and convert them to arrays of note timing and pitches that are then played by the teensy. Using the Teensy 3.2's three independent clocks to vary PWM frequency on three output pins, 3-voice music (Mario, Zelda, Tetris) can be played.

The video above uses piezos to show simplicity but I have tried it using three small [amplifier PCBs](https://oshpark.com/projects/DPx0NZIw), speakers, and volume control.


#### Links:
* [Github page](https://github.com/bkeegs/chiptune_teensy) includes python for midi to timing conversion, and C code for the teensy.
* All midi files used are from [http://www.khinsider.com/midi](http://www.khinsider.com/midi) and are not my own.
