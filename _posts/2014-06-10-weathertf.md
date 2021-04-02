---
layout: post
title: "WeatherTF"
description: "Rails app to warn you of rain"
---
_{{ page.description }}._ [[github](https://github.com/dtredger/weathertf)]

WeatherTF is a simple rails app that sends you an SMS message with the forecast for your latitude/longitude every 
morning . Lat/Lon is determined by browser geolocation (if available).

Messages are actually just emails, which are sent to your carrier's `SMS gateway`, which will deliver a plain-text 
email as a message. Messages are sent at 8am (EST) every morning via resque-scheduler. Normal emails are sent using resque.

* Forecasts are via the Forecast.io. API.
* Background images are from Ansel Adams' _"National Parks"_ series). 

`app not currently deployed anywhere`
