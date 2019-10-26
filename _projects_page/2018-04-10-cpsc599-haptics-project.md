---
layout: article
title: Haptics Project
key: 20180410
permalink: /projects/haptics-project
cover: assets\images\Projects\Haptics\Project\icon.png
aside:
  toc: true
article_header:
  type: cover
  image:
    src: assets\images\Projects\Haptics\Project\demo.png
---

Course project for the *Computer Haptics* course (Computer Science 599.86 at the University of Calgary) I took in winter 2018. 

<!--more-->

Sadly I no longer have access to the Novint Falcon haptic devices used in this course so I cannot take screenshots or record videos demoing the haptic components of this project. Even worse, I can no longer run this project so I cannot get any new screenshots of it. Fortunately I have a screenshot and video from when I worked on this project but they're both really low quality. Although haptics really are something you just have to feel yourself so screenshots and videos wouldn't do it justice anyway. 

###### Source code is self-hosted on my home Git-Gogs server which is only accessible from my home network.

--- 

# Project Summary

## Objective

Implement haptics within Unreal Engine 4 using CHAI3D as a driver.

## Features
- Haptic device controlled a sphere in the scene.
- Forces were sent back to the haptic device allowing for haptic feedback.
- Used the god object algorithm to keep the haptic cursor from pushing through an object.
  - One sphere directly controlled by the haptic device.
  - The other sphere would follow the haptic controlled sphere while obeying collisions. 
  - Had a virtual "spring" connecting the two.
- Used multiple threads for haptics to feel better.
- Created a simple demo scene where you could push stuff around.

## Challenges
- First time using UE4 from a programing perspective.
- Only had about a month to complete the entire project and I was working independently.
- UE4's build system took a while to figure out.
  - Changed my approach at least half a dozen times before finally figuring out how to not only get input from but also send information to the haptic device.
- Despite the haptic sphere updating at 1000hz, the collision sphere was locked with the game's framerate.
  - This was because UE4's collisions were only being checked every frame and I was not skilled enough to figure out a way to fix this without rewriting the collision system on my separate thread.
  - Still felt somewhat okay and it was rather fun to throw around dynamic objects with haptic feedback.
  
## Credits
- [CHAI3D Haptics library](https://www.chai3d.org/).
- Related project [Karaage](https://github.com/bhnascar/Karaage) which I used as a basis for figuring out how to get everything working while using newer versions of CHAI3D and UE4.
- [Custom input device plugin guide](https://wiki.unrealengine.com/Custom_input_device_plugin_guide) on Unreal Engine 4's wiki.
- [Multi-Threading guide](https://wiki.unrealengine.com/Multi-Threading:_How_to_Create_Threads_in_UE4) on Unreal Engine 4's wiki.
  
# Demo
## Screenshot
<img src="\assets\images\Projects\Haptics\Project\demo.png" width="100%" />
Basically the final version except all the objects were made dynamic in the final scene and I added walls to keep the user from knocking stuff off into infinity.

<img src="\assets\images\Projects\Haptics\Project\icon.png" width="100%" />
UE4 generated icon for the project which somewhat shows off the final scene where everything except for the walls and floor was dynamic and could be thrown around with full haptics.

## Video
<div style="position:relative;padding-top:56.25%;">
  <iframe src="https://www.youtube.com/embed/i4uZjRIw1SY"  frameborder="0" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;"></iframe>
</div>
This was for the milestone presentation where I only got the haptic device hooked up as a controller and was not getting any haptic forces back to the device. 

--- 