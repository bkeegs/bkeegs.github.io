---
layout: post
title:  "Chiptune Teensy"
date:   2017-02-07 11:31:45 -0800
categories: hardware_projects
---

<iframe width="560" height="315" src="https://www.youtube.com/embed/vXwI87gkwMY" frameborder="0" allowfullscreen></iframe>

<br>

It's not music to everyone's ears, but to me this old "chiptune" music has a certain nostalgia to it.

This hack was designed as a minimal chiptune player using just a Teensy 3.2 and 3 piezoelectric buzzers. Using the Teensy's independent clocks to vary PWM frequency on three output pins, music (Mario, Zelda, Pokemon, etc.) can be played. Each output pin provides a square-wave that controls pitch and timing for one "voice," so only one note is played by each piezo at a given time.

This project uses vishnubob's [python-midi](https://github.com/vishnubob/python-midi) library to parse midi files and convert them to arrays of note timing and pitches. The same python script then generates a .ino file that can be flashed directly to the teensy.

The video above uses piezos to show simplicity but I have tried it using three small [amplifier PCBs](https://oshpark.com/projects/DPx0NZIw), speakers, and volume control. It sounds a bit better, mainly due to the piezo's frequency response  

<br>

#### Links:
* [Github page](https://github.com/bkeegs/chiptune_teensy) includes python for midi to timing conversion, and generated C code for the teensy.
* All midi files used are from [http://www.khinsider.com/midi](http://www.khinsider.com/midi) and are not my own.
* For midi to .wav conversion, I used Coolsoft's [VirtualMidiSynth](http://coolsoft.altervista.org/en/virtualmidisynth).
* [MidiEditor](http://midieditor.sourceforge.net/) is the software that was used for all midi editing. A few of the midis used needed light doctoring to simplify parsing rules in the python script. For example, the wild pkmn battle.midi and prof_oaks_lab.midi both had duplicate notes that needed removing (within one voice, two notes of same frequency and start time). The Zelda overworld midi originally had 6 voices, but with a bit of tailoring this was brought down to 3 without removing much actual content.
