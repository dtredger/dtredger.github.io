---
layout: post
title: "Bird Friend"
description: Animatronic Birds with Python
image: "crow-friend.webp"
image_2: "yellow-bird.webp"
order: 4
---

_{{ page.description }}_ [[github](https://github.com/dtredger/bird_friend)]

This repository is code for a series of different animatronic birds, built with Raspberry Pi (standard and Pico) and coded with Python (and MicroPython).

There are currently 4 different bird models:

#### 1) Paper-Mache crow (Pictured above)
- Neck motion, Beak motion, Audio (caws the hour of the day)

#### 2) Yellow Bird (Below)
- Neck motion, Light-up eyes, Audio (chirps while neck moving)

#### 3) "Edgar" (realistic Black Crow)
- Neck motion, Light-up eyes, Audio (caws the hour of the day), Wireless access point (for configuration)

#### 4) "Ronny" (Blue Parrot)
- Neck motion, Light-up eyes

---

![]({{ page.image_2 | prepend: '/assets/images/' | prepend: site.baseurl | prepend: site.url }})

Since each bird has different capabilities, and is based on a different platform (whether Raspberry Pi standard, Pico, or Adafruit Feather), not much code is shared.
In the future it would be valuable to standardize a bit more.

Also, currently most of the animation is time-based, which was _not_ the goal I began with. I'd prefer for the animation to be much more random and less useful as a clock.
