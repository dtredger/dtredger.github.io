---
layout: post
title: "Basement Machine Learning"
description: "A Pytorch Model of inside temperature in Winter"
---

_{{ page.description}}_ [github]()

This Repo takes a month of temp and humidity sensor readings and attempts to create a model to predict future temperatures. The data was collected from sensors running on a Raspberry Pi, with code for that system 
<a href="{{'/projects/raspberry-pi' | prepend:site.baseurl}}">available here</a>.

The model is written with **_Pytorch_** as a **_Jupyter Notebook_**, so there is extensive documentation about how 
it works there