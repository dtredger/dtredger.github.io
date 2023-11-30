---
layout: post
title: "Raspberry Pi"
description: 3 Raspberry Pi Repos (Webserver, Sensors, and FM Radio)
image: "raspberry_pi_graph.jpg"
---

_{{ page.description }}_ [[github](https://github.com/dtredger/RaspberryPI)]

1) **webserver_pi**

   Tornado or Flask webserver
   A tornado app that serves data from other parts of the Raspberry pi. Also still has a crude front-end, and a tool to one-line text (useful for command-line sql). running directly on the raspberry pi (visit here). Filter the graph data by adding a number to the data returned, ie: /graph/10 returns the 10 most-recent data-points.


2) **humidity_pi**

   Humidity and Temperature Logger
   The temp/humidity logger relies on a c program (from Adafruit) to read a DHT-22 sensor attached to the Raspberry Pi's GPIO pins. Python writes the returned sensor data, either to an sqlite database, or to a csv one line at a time. Reads the sensor every 3 seconds, but takes a command-line option for how often to write (if set to write every hour, averages readings for that hour).


3) **radio_pi**

   FM Radio transmitter. Uses the pifm binary to transmit .wav audio over FM radio using the Rasperry Pi's GPIO pins.

   Python code creates playlists from folders of music, can set shuffle or continuous play. For files that are not in .wav format, it uses ffmpeg to convert, and streams this file (which is in fact written to dev/null!). The broadcast is currently set to 101.1 FM, but can only be heard a few meters away.
