---
layout: post
title: "Sailing Speed Calculator"
description: "Calculations and graphs of sailing VMG vs TWA"
image: "imoca_polar.jpg"
---

_{{ page.description }}_ [[github](https://github.com/dtredger/vmg-calculator/blob/master/vmg_calculator.ipynb)]

This repository is a **_Jupyter Notebook_** containing basic calculations of **Velocity Made Good (VMG)** for the most
efficient way to sail to a given destination.

The notebook also includes wind polars for a **Figaro 3** and generic **2015 Imoca** (from qtVlm), as well as a generic
wave polar (which shows percent of best performance achievable in a given sea-state).

While the polar data is boat-specific, I also calculate the required extra speed to make a decision to bear off
viable. For example:
> increasing TWA from 40º to 45º will increase the distance sailed by over **8%**.

So in the above case, unless bearing off will increase boatspeed by > 8%, VMG will actually be worse, despite an
increase in speed.
