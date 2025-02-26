---
layout: article
title: Portable NPK Soil Sensor - Unfinished
key: 20210820
permalink: /projects/npk-soil-sensor
cover: "/assets/images/Projects/NPKSensor/Icon.jpg"
aside:
  toc: true
article_header:
  type: cover
  image:
    src: "/assets/images/Projects/NPKSensor/Banner.jpg"
---

Sensor for detecting nitrogen, phosphorus, and potassium in garden soil. Current status: Abandoned in a functional but nonportable state.

<!--more-->

##### [Source code](https://github.com/Beskamir/npkSensor)

--- 
# Project Summary

## Objective

Make a durable and portable NPK sensor I can use in the garden.

## Justification
- I was getting into gardening at the time and wanted to test my soil.
- Learning opportunity to program and wire an Arduino project.

## Features
- Displays nitrogen, phosphorus, and potassium values from a NPK sensor to an OLED screen.

## Challenges
- Figuring out a portable power source delayed this project for years.
  - This is the reason why this project is currently unfinished.
  - I have this solved now after finding a small and portable 9v power supply, but my interest in this project has since passed.
- The Arduino Nano I was using for this project had only a few KBs of memory.
  - Had to slim my code down to only what was absolutely necessary.
- I discovered that the tutorial I was following made a mistake and only used one byte of data from a two byte value.
  - Meaning, my tests were making absolutely no sense and I had no idea what was happening until I finally managed to make sense of the manual.
  - Since then this seems to have been corrected in several newer tutorials and the manual I found online while writing up this brief report looks a lot less confusing than what I had available at the time of making this project.
- Feature creeping this project into a tutorial on how to build such a device yourself when I should have just wrapped it up and then written a very brief description like the one you're currently reading.

## Lessons learned
- Do not finalize enclosures until the entire project is completed.
- Do not blindly trust tutorials to always be correct.
- Even for a seemingly simple project it's always best to be aware of hardware limitations at the start of the project.

## Improvements
- Switching to an E-Ink display.
  - Much lower power consumption than an OLED.
  - Not as pretty, but that doesn't matter for this project.
- Finally get around to actually wiring up the portable 9v battery and designing a new enclosure so that this project can be considered finished.

--- 

# Screenshots

## Work in progress pictures
<img src="/assets/images/Projects/NPKSensor/Banner.jpg" width="100%" />
<img src="/assets/images/Projects/NPKSensor/WIP.jpg" width="100%" />
<img src="/assets/images/Projects/NPKSensor/Wiring.png" width="100%" />
<img src="/assets/images/Projects/NPKSensor/Housing.jpg" width="100%" />


# Videos

## A simple test video I took for my girlfriend at the time
<div style="position:relative;padding-top:56.25%;">
  <iframe src="https://www.youtube.com/watch?v=sdmqfec8fos" frameborder="0" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;"></iframe>
</div>

---

# Credits
## Tutorials
- [The tutorial I followed for this project](https://how2electronics.com/measure-soil-nutrient-using-arduino-soil-npk-sensor/). This had to be fixed since that code is only returning one of the two byte of data.

## Third Party Libraries
- [Code for getting the OLED to work](https://arduinogetstarted.com/tutorials/arduino-oled). This had to be considerably slimmed down due to hardware limitations.

---

