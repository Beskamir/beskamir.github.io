---
layout: article
title: RTX Rendering Project
key: 20190410
permalink: /projects/rendering-project
cover: https://cdnb.artstation.com/p/assets/images/images/017/564/095/large/sebastian-kopacz-template-2019-04-28-20-12-27.jpg?1556505732
aside:
  toc: true
article_header:
  type: cover
  image:
    src: https://cdnb.artstation.com/p/assets/images/images/017/564/095/large/sebastian-kopacz-template-2019-04-28-20-12-27.jpg?1556505732
---

Course project for the _Rendering_ course (Computer Science 591 at the University of Calgary) I took in winter 2019 and where I implemented ray tracing that made use of Nvidia's RTX hardware through the Vulkan API.

<!--more-->

[ArtStation Link](https://www.artstation.com/artwork/zA0a0L)

###### Source code is self-hosted on my home Git-Gogs server which is only accessible from my home network.

--- 
# Project Summary

## Objective

Learn the Vulkan basics and implement ray tracing that is accelerated by Nvidia's RTX hardware. 

## Justification
- Just seemed like the coolest project idea I could think of that didn't necessarily require a load of math.
- It was a massive learning opportunity!
  - Went in not knowing Vulkan, came out at least knowing the basics.
  - This also translated to a better understanding of OpenGL and graphics APIs in general.
  - Learned how to implement RTX.
  - Got to experiment with RTX before it was supported by everything.
- Self-justification...
  - I bought a RTX2080 very shortly after launch and had to somehow justify the early adopter fee.
  
## Features
- Normal Vulkan rasterization with z-fighting. 
  - This wasn't the main objective so I didn't care enough to fix it.
- Ray tracing using RTX in Vulkan. 
  - Unfortunately only got direct lighting and simple shadows implemented.
- Expected window options supported like resizing or minimizing the window are supported.
- Can switch between rasterized and ray traced views.
- User specified camera movement with the ability to unlock the mouse so you can take screenshots or resize the window.

## Challenges
- Learning Vulkan and how to implement RTX at the same time. 

--- 

# Screenshots

## Ray Tracing
### Final version
<img src="https://cdnb.artstation.com/p/assets/images/images/017/564/095/large/sebastian-kopacz-template-2019-04-28-20-12-27.jpg?1556505732" width="800" />
<img src="/assets/images/Projects/Rendering/Project/raytracerFinal(1).png" width="800" />

### WIP renders
<img src="/assets/images/Projects/Rendering/Project/raytracerFinal(2).png" width="800" />
<img src="/assets/images/Projects/Rendering/Project/rayTracerTests(3).png" width="800" />
<img src="/assets/images/Projects/Rendering/Project/rayTracerTests(1).png" width="800" />

## Rasterization
<img src="https://cdna.artstation.com/p/assets/images/images/017/564/096/large/sebastian-kopacz-template-2019-04-28-20-12-37.jpg?1556504005" width="800" />
<img src="/assets/images/Projects/Rendering/Project/rasterization(1).png" width="800" />
<img src="/assets/images/Projects/Rendering/Project/rasterization(3).png" width="800" />
<img src="/assets/images/Projects/Rendering/Project/rasterization(2).png" width="800" />
<img src="/assets/images/Projects/Rendering/Project/rasterization(4).png" width="800" />

# Videos

## Ray Tracing
<iframe width="775" height="475" src="https://www.youtube.com/embed/GeCFv7IaF_Y" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<iframe width="775" height="475" src="https://www.youtube.com/embed/5wluZLteb8c" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Rasterization
<iframe width="775" height="475" src="https://www.youtube.com/embed/TX_6Z4EneaE" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

---

# Credits
## Vulkan Resources
- [Alexander Overvoorde's Vulkan-Tutorial](https://vulkan-tutorial.com/).
- [Sascha Willems's Vulkan Examples and Demos](https://github.com/SaschaWillems/Vulkan).
- [Vulkan API and Documentation](https://vulkan.lunarg.com/doc/view/latest/windows/apispec.html).

## RTX Resources
- [Martin-Karl Lefrançois and Pascal Gautron's Vulkan RTX Tutorial on Nvidia's blog](https://developer.nvidia.com/rtx/raytracing/vkray).
- [Sergii Kudlai's Vulkan RTX Tutorial](https://iorange.github.io/p01/HappyTriangle.html).

## General Credits
- The event system, logger, and window startup are all based on early versions of [Yan Chernikov's Hazel game engine](https://github.com/TheCherno/Hazel) since I was following his game engine series around the time of this project.

---
