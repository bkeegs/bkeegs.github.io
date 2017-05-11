---
layout: post
title:  "Chiptune Teensy"
date:   2017-02-07 11:31:45 -0800
categories: hardware_projects
---

<iframe width="560" height="315" src="https://www.youtube.com/embed/vXwI87gkwMY" frameborder="0" allowfullscreen></iframe>

<br>

It's not exactly easy listening, but this old chiptune music has a certain nostalgia to it.

This hack was designed as a minimal chiptune player using just a Teensy 3.2 and 3 piezoelectric buzzers. Using the Teensy's internal clocks to vary PWM frequency on three output pins, music (Mario, Zelda, etc.) can be played. Each output pin provides a square-wave that controls pitch and timing for one "voice," so only one note is played by each piezo at a given time.

This project uses vishnubob's [python-midi](https://github.com/vishnubob/python-midi) library to parse midi files and convert them to arrays of note timing and pitches. The same python script then generates a .ino file that can be flashed directly to the teensy.

The video above uses piezos but I have tried it using three small [amplifier PCBs](https://oshpark.com/projects/DPx0NZIw), speakers, and volume control.

Because most of the Teensy's PWM outputs are tied to the same internal clock (see section on PWM Frequency [here](https://www.pjrc.com/teensy/td_pulse.html)), I needed to access a pad on the bottom of the board in order to have three separate frequencies output simultaneously. A picture of this is below:

![Solder to Pin 25]({{ site.url }}/assets/images/chiptune/chiptune_mod_small.JPG)

<br>

#### Links:
* [Github page](https://github.com/bkeegs/chiptune_teensy) includes python for midi to timing conversion, and generated C code for the Teensy.
* All midi files used are from [http://www.khinsider.com/midi](http://www.khinsider.com/midi) and are not my own.
* For midi to .wav conversion, I used Coolsoft's [VirtualMidiSynth](http://coolsoft.altervista.org/en/virtualmidisynth).
* [MidiEditor](http://midieditor.sourceforge.net/) was used for basic midi editing.
