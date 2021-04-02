---
layout: post
title: "Antipodes"
description: "Find the city furthest from you"
---

_{{ page.description }}._ [[github](https://github.com/dtredger/antipodes){:target="_blank"}]

Antipodes is an angular-based site that finds your antipode, and the closest city to there; ie: _the city 
farthest from you._

The site takes your latitude/longitude from browser geolocation, then calculates the geographic antipode, and centers a mapbox map on that location.

Technologies/Services Used:
------------
* Angular 1
* Webworkers
* Papaparse.js
* Mapbox

From that point, the site can find the closest city by comparing your anti-coordinates to a 90mb csv. The csv is a list of cities and their latitude/longitude, and I use the papaparse.js library to churn through them, saving the closest one. Webworkers read the csv so the browser tab remains interactive. An angular directive shows a progress bar of parsing status (updated every 5% complete).

Since everything happens client-side, there is no need for a server. The one catch with this solution is that every find requires downloading the entire coordinates file. Given transfer fees for file hosting, it's probably cheaper to do this on a server (v_v;)

Issues:
------------
Currently, calculation of the closest city is inaccurate, since it assumes lines of latitude are the same distance 
apart as lines of longitude (not true), and assumes that lines of longitude are always the same distance apart (also not true). The solution is to calculate the **Haversine Distance** between points (this is implemented in <a href="{{'/projects/tba-kite-site' | prepend: site.baseurl}}" target="_blank">TBA Kite Site</a>)
