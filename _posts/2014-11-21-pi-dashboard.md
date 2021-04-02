---
layout: post
title: "piDashboard"
description: 'Angular dashboard for sensor data'
---

_{{ page.description }}._ [[github](https://github.com/dtredger/pidashboard){:target="_blank"}]

piDashboard is based on rDash Dashboard . The site is an angular-based dashboard for data provided by a Raspberry Pi. 
(see <a href="{
{'/projects/raspberry-pi' | prepend: site.baseurl}}" target="_blank">RaspberryPi</a> for code for running 
sensors).

Currently the site has two functions-ish:

* Display a carousel of timelapse images captured by a raspberry pi. 
* Show a graph of temp/humidity recorded by a raspberry pi 
  
A crude live version of the site was being served by nginx running on a raspberry pi (the same pi as provides the data), but this was too much of a drain on resources (in the event someone visited).

Issues
---------

* A Carousel isn't a good way to show timelapse images (many of which are pitch-dark...), but the raspberry pi is too constrained to do video-processing
* The humidity graph shows all data-points (it has no ability to date-filter for recency).