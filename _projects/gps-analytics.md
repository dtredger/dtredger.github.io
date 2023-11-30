---
layout: post
title: "GPS Analytics"
description: "Analysis of sailing GPS traces"
image: "gps-analytics.png"
date: 2023-10-20
---

_{{ page.description }}_ [github](https://github.com/dtredger/gpx-analytics)

This repository is a **_Jupyter Notebook_** that accepts a GPX file or CSV of GPS locations and maps and analyzes the result.

The code analyzes tacking/gybing angles and infers a wind direction based on them. From that, we can calculate VMG.

The data is mapped, colour-coded by tack and whether upwind or downwind. Points on the map can be scrubbed through using the speed chart below.

In addition, we can generate:

##### Violin Plot
 a chart of the angles sailed between each maneuver.
 This allows comparing tacking angles, but also different multiple tacks or gybes on the same leg

##### Polar Plot
Shows avg and 90th percentile speed at every given compass angle. The data can also be filtered (in the event the wind shifts).   
