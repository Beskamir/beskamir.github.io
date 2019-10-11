---
layout: article
title: Top Hat Notification Script
key: 20190527
permalink: /projects/top-hat-notification
# cover: https://cdnb.artstation.com/p/assets/images/images/017/564/095/large/sebastian-kopacz-template-2019-04-28-20-12-27.jpg?1556505732
aside:
  toc: true
# article_header:
#   type: cover
#   image:
#     src: /assets/images/cover1.jpg
---

Simple Python script to notify me when Top Hat question are up so I could skip high school physics review (aka Physics 221 at the University of Calgary) lectures.

<!--more-->

**Warning: Since this program helps you skip class, I've intentionally ensured some competence is needed to make use of it. As such this documentation, while complete, will not hold your hand. Also this script is by no means perfect (might have false positives/negatives) and relies on a command line interface. These are missing features that have been left for whoever wants to make use of this to skip lectures to fix or implement.**

#### [Source code](https://github.com/Beskamir/TopHatNotify.git)

---

# Features
 - Works with multiple Top Hat courses.
 - Plays notification sound (notifySound.wav).
 - Prints notification to console.
 - On Windows, sends a proper Windows notification.

---

# Setup and Install

## Clone the repository
    git clone https://github.com/Beskamir/TopHatNotify

## Setup your config.ini file
 - Rename `sampleConfig.ini` to `config.ini` 
 - Fill it with:
   - Your Top Hat credentials.
   - The Top Hat urls you want it to check.

## Install the necessary libraries 
(some of these should be installed by default but I'll list them anyway)

    pip install selenium
    pip install playsound
    pip install win10toast
    pip install typing
    pip install time
    pip install configparser
    pip install json
    pip install os

## Run the Python file
    py -3 .\Notify.py

---

# Platform/Python Requirments
 - Developed and tested on Windows 10.
 - Should be cross-platform except for win10toast.
   - Use a different library or disable that feature if you're not on windows.
 - Uses Python 3 but it might be compatible with Python 2.

# Known issues
 - Might have some false positives or worse negatives.
 - Might crash every so often.
 - Basically works about 95% of the time! (Which for me that was more than good enough)

# Nice to have features 
(that I don't care enough to implement so they're left as an exercise to the user)
 - Different notification sound for first message vs reminders
 - Time stamp the notifications when printing them to the console
 - Ability to dismiss or turn off the notification reminders 

---