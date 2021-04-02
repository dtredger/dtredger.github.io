---
layout: post
title: "Generative Music"
description: "Generate MIDIs from data"
---

_{{ page.description }}._ [[github](https://github.com/dtredger/generative-music){:target="_blank"}]

This repo takes data and transforms it into midi files (uses midiutil library). MIDI files are then transformed into 
**_.wav_** audio with fluidsynth and a soundfont. 

Currently the transformation of the input data is a basic linear transformation. In my case, the data is from temp 
and humidity sensors running on a Raspberry pi. The <a href="{{'/projects/raspberry-pi' | prepend: site.baseurl}}
">RaspberryPi</a> repo shows an example of source data.

That same <a href="{{'/projects/raspberry-pi' | prepend: site.baseurl}}">repo</a> also has code to  
create a hyperlocal FM radio station that can broadcast media files.

Playing Sounds:
------------

To play the music, you will need:
* The ability to play MIDI files (it appears Mac OS can no longer play MIDI files by default. You'll need 
  **_FluidSynth_** (you can brew install fluid-synth. 
* A **_Sound Font_** to actually play the MIDI file (you can chose which instrument). I've included an open-source 
  piano 
  in the repo: there are tons of instrument options out there.

The most up-to-date code is in the `feature/csv_readings` branch.