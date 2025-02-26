---
layout: article
title: Raytracing and Deferred Render Engine
key: 20190322
permalink: /projects/rendering-assignments
cover: https://cdna.artstation.com/p/assets/images/images/017/563/376/large/sebastian-kopacz-starsonly-5.jpg?1556500064
aside:
  toc: true
article_header:
  type: cover
  image:
    src: https://cdna.artstation.com/p/assets/images/images/017/563/162/large/sebastian-kopacz-wasteland.jpg?1556498859
---

Various assignments I did for the Rendering course (Computer Science 591 at the University of Calgary) I took in winter 2019.

<!--more-->

##### Links to additional images on my ArtStation
- [Test for BVH vs KD trees in PBRT](https://www.artstation.com/artwork/N5gAaP)
- [Polygonal apertures in PBRT](https://www.artstation.com/artwork/A960v5)
- [Deferred rendering in OpenGL](https://www.artstation.com/artwork/nQvA2X)
- [SSAO in OpenGL](https://www.artstation.com/artwork/RYgAXy)

###### Source code is self-hosted on my home Git-Gogs server which is only accessible from my home network.

---
# BVH vs KD

## Features
- Made the test scene in Blender then figured out how to export it to PBRT and automate as much of the process as possible.
- I then just added models to a selected region in the scene and had a batch script rendering each scene with PBRT using both KD and BVH acceleration.
- Once that was done all that was needed was to graph the results and realize that both increase at the same rate with just a slight difference in speed.

### Cycles Render
<img src="https://cdna.artstation.com/p/assets/images/images/017/563/162/large/sebastian-kopacz-wasteland.jpg?1556498859" width="100%" />

### PBRT Render
<img src="https://cdna.artstation.com/p/assets/images/images/017/563/130/large/sebastian-kopacz-as-test.jpg?1556498758" width="100%" />

#### Examples of the test objects I added to the scene
<img src="/assets/images/Projects/Rendering/Assignments/ExampleModel.png" width="100%" />
<img src="/assets/images/Projects/Rendering/Assignments/ExampleObjects.png" width="100%" />

### Comparison Graph
<img src="/assets/images/Projects/Rendering/Assignments/Graph-2019-10-06_01-00-40.png" width="100%" />
Increase in render time as the number of test objects in the scene increases. Both time increases are clearly logarithmic as they barely increase while the 𝑥-axis is exponential. Which matches the literature time complexity (𝑂(log(𝑛)) for BVH and KD Trees. Rendered using an AMD Threadripper 1950x.

## Credits
- [PBRT library](https://github.com/mmp/pbrt-v3) and the corresponding documentation. 

---
# Polygonal Apertures

## Features
- By default PBRT only has circular apertures.
- Extended PBRT to support any regular polygonal aperture.
- Also supports stars of any polygonal number of points despite the bonus only requiring 5 pointed stars.

### Default PBRT Aperture
<img src="https://cdna.artstation.com/p/assets/images/images/017/563/324/large/sebastian-kopacz-starsonly0.jpg?1556499678" width="100%" />

### Regular 5-Sided Aperture
<img src="https://cdnb.artstation.com/p/assets/images/images/017/563/375/large/sebastian-kopacz-starsonly5.jpg?1556499973" width="100%" />

### 5-Point Star Aperture
<img src="https://cdna.artstation.com/p/assets/images/images/017/563/376/large/sebastian-kopacz-starsonly-5.jpg?1556500064" width="100%" />

#### Regular triangle aperture
<img src="https://cdnb.artstation.com/p/assets/images/images/017/563/327/large/sebastian-kopacz-starsonly3.jpg?1556499680" width="100%" />

#### 3-Point Star Aperture
<img src="https://cdna.artstation.com/p/assets/images/images/017/563/330/large/sebastian-kopacz-starsonly-3.jpg?1556499790" width="100%" />

## Credits
- [PBRT library](https://github.com/mmp/pbrt-v3) and the corresponding documentation. 

---
# Sampling Fix

PBRT has a bug where it will sample a half disk the same as a full disk, our task was to fix this by changing the samples so that it would be from just the half disk rather than the entire disk. Unfortunately I used rejection sampling instead of properly transforming the samples to be uniformly spaced on the disk. As such my implementation was incorrect and visually unimpressive.

## Features
- Uses rejection sampling to ignore invalid rays.

### The issue
<img src="/assets/images/Projects/Rendering/Assignments/Ring360-old.png" width="100%" />

### My horrible fix
##### (Note how the brightness decreases due to rejection sampling)
<img src="/assets/images/Projects/Rendering/Assignments/Ring360.png" width="100%" />
<img src="/assets/images/Projects/Rendering/Assignments/Ring180.png" width="100%" />
<img src="/assets/images/Projects/Rendering/Assignments/Disk270.png" width="100%" />

## Credits
- [PBRT library](https://github.com/mmp/pbrt-v3) and the corresponding documentation. 

---
# Deferred Rendering

## Features
- Based on my model viewer from _[Intro to Computer Graphics](http://localhost:4000/projects/Intro-to-Graphics)_.
   - As such shares many of the features that were implemented for that assignment.
- Main addition is the deferred rendering pipeline.
- Also has Oren-Nayer diffuse shading in addition to Phong shading.
  
### Phong lighting
<img src="https://cdna.artstation.com/p/assets/images/images/017/563/704/large/sebastian-kopacz-assignment4-2019-04-28-19-40-00.jpg?1556502324" width="100%" />

### Oren-Nayer shading
##### Sigma = 0
<img src="https://cdna.artstation.com/p/assets/images/images/017/563/706/large/sebastian-kopacz-2019-04-28-19-40-07.jpg?1556502069" width="100%" />

##### Sigma = 20
<img src="https://cdna.artstation.com/p/assets/images/images/017/563/708/large/sebastian-kopacz-2019-04-28-19-40-36.jpg?1556502076" width="100%" />


## Credits
- [Learn OpenGL](https://learnopengl.com/) has always been my go to source for anything OpenGL related and this was no different.
- Following resources helped with figuring out Oren-Nayer shading
   - [http://www.sidefx.com/docs/houdini/nodes/vop/oren.html](http://www.sidefx.com/docs/houdini/nodes/vop/oren.html)
   - [http://jship.github.io/glPortfolio/demos/oren_nayar/oren_nayar.html](http://jship.github.io/glPortfolio/demos/oren_nayar/oren_nayar.html)
   - [https://en.wikipedia.org/wiki/Oren%E2%80%93Nayar_reflectance_model](https://en.wikipedia.org/wiki/Oren%E2%80%93Nayar_reflectance_model)

---
# SSAO
  
## Features
- Continuation of the previous assignment (assignment 4, deferred rendering) so many of the previous features carried over.
- Implemented Crytek's SSAO
- Rocket model was a slightly upgraded version of the rocket in the scene for assignment 1.

### Without SSAO
<img src="https://cdnb.artstation.com/p/assets/images/images/017/563/975/large/sebastian-kopacz-2019-04-28-20-02-46.jpg?1556503414" width="100%" />

### With SSAO
<img src="https://cdnb.artstation.com/p/assets/images/images/017/563/967/large/sebastian-kopacz-assignment5-2019-04-28-20-02-39.jpg?1556503650" width="100%" />

## Credits
- Once again [Learn OpenGL](https://learnopengl.com/) has helped me figure stuff out.

---
