---
layout: article
title: Karsio Engine and Game
key: 20180320
permalink: /projects/Karsio
cover: https://cdna.artstation.com/p/assets/images/images/021/123/064/large/sebastian-kopacz-2019-10-05-23-11-04.jpg?1570477476
aside:
  toc: true
article_header:
  type: cover
  image:
    src: https://cdna.artstation.com/p/assets/images/images/021/123/064/large/sebastian-kopacz-2019-10-05-23-11-04.jpg?1570477476
---

Group course project for the _Games Programming_ course (Computer Science 585 at the University of Calgary) I took in winter 2018 and where I worked in a team of 4 (Ben, Rukiya, Brian, and myself) to build a game engine and of course the game itself.

<!--more-->

<!-- ##### Links to additional images on my ArtStation:
- [Test for BVH vs KD trees in PBRT](https://www.artstation.com/artwork/N5gAaP)
- [Polygonal apertures in PBRT](https://www.artstation.com/artwork/A960v5)
- [Deferred rendering in OpenGL](https://www.artstation.com/artwork/nQvA2X)
- [SSAO in OpenGL](https://www.artstation.com/artwork/RYgAXy) -->

[Link to source code](https://github.com/Beskamir/KarsioVS)

--- 

# Project Summary:

## Objective:

Make a driving game within a semester in a team of 4 computer science majors.

## Allowed Libraries:
- Microsoft DirectX
- Glut
- **Glew**
- **OpenGL Mathematics (GLM)**
- **PhysX SDK**
- Open Dynamics Engine
- Simple DirectMedia Layer
- OpenAL
- **Fmod**
- Cg Toolkit
- **OpenGL Extension Wrangler Librar (glfw)**
- **FTGL Font Library**
- **Open Asset Importer Library (assimp)**
- **stb**

The libraries we used are indicated with **bold text**.

## Our Idea:

Battle royal driving game blended with [slither.io](http://slither.io/)'s growth concept. 

## Features:
- Upgrade system.
  - Chassis: 
    - Unlocks higher level upgrades but makes you larger and slows you down.
  - Gun: 
    - Ranged weapon deals more damage or fires faster.
  - Armor: 
    - Take less damage when hit.
  - Ram: 
    - Deal more damage when ramming your enemies.
- Resource crystals.
  - Blue crystals needed for upgrades.
  - Red crystals restore health.
- AI makes use of crystals and upgrades.
- Sound effects and music.
- Procedural level.
- Lock on targeting.
- Custom art assets.
- Entity component system for entity organization.
- Uses Nvidia PhysX for collisions and driving model.
- Keyboard and Xbox controller supported.

## My Tasks:

### Render Engine:
- 2D user interface rendering class.
  - FreeType text.
  - Image planes.
- 3D renderer for currently active models.
  - PBR materials.
  - Shadow mapping using a central point light.
  - Crystals slightly change color based on the user's view to create a sparkle effect.
  - Space skybox which can be best seen on the main menu.
- GLFW window setup.

### Art Import System:
- Parse .ini files to find art assets.
- Models loaded using assimp.
- Textures loaded using stb.
- Shaders compiled and readied.

### Credits:
- My excellent team members Ben, Rukiya, and Brian.
- [LearnOpenGL](https://learnopengl.com/) for helping me figure out how to use OpenGL.
- Space skybox generated using [Spacescape](http://alexcpeterson.com/spacescape/).

---

# Gameplay Video:

<iframe width="775" height="425" src="https://www.youtube.com/embed/cg6CkGn4yRI" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
For some reason audio wasn't recorded (and it may be copyrighted anyway) so for the full effect, get the game on GitHub and compile it yourself.

# Artwork:

## Ingame Screenshots:
<img src="https://cdna.artstation.com/p/assets/images/images/021/123/064/large/sebastian-kopacz-2019-10-05-23-11-04.jpg?1570477476" width="800" />
<img src="https://cdnb.artstation.com/p/assets/images/images/021/123/067/large/sebastian-kopacz-2019-10-05-20-36-31.jpg?1570477214" width="800" />
<img src="https://cdna.artstation.com/p/assets/images/images/021/123/054/large/sebastian-kopacz-2019-10-05-20-36-41.jpg?1570477204" width="800" />
<img src="https://cdnb.artstation.com/p/assets/images/images/021/123/059/large/sebastian-kopacz-2019-10-05-20-37-33.jpg?1570477206" width="800" />
<img src="https://cdna.artstation.com/p/assets/images/images/021/123/062/large/sebastian-kopacz-2019-10-05-20-39-04.jpg?1570477209" width="800" />
<img src="https://cdnb.artstation.com/p/assets/images/images/021/123/065/large/sebastian-kopacz-2019-10-05-20-39-36.jpg?1570477211" width="800" />
<img src="https://cdna.artstation.com/p/assets/images/images/021/123/068/large/sebastian-kopacz-2019-10-05-20-39-51.jpg?1570477214" width="800" />
<img src="https://cdnb.artstation.com/p/assets/images/images/021/123/061/large/sebastian-kopacz-2019-10-05-20-41-08.jpg?1570477209" width="800" />
<img src="https://cdna.artstation.com/p/assets/images/images/021/123/056/large/sebastian-kopacz-2019-10-05-20-39-57.jpg?1570477473" width="800" />
<img src="https://cdna.artstation.com/p/assets/images/images/021/123/058/large/sebastian-kopacz-2019-10-05-20-40-20.jpg?1570477207" width="800" />
<!-- <img src="/assets/images/Projects/Karsio/2019-10-05_23-11-04.png" width="800" />
<img src="/assets/images/Projects/Karsio/2019-10-05_20-36-31.png" width="800" />
<img src="/assets/images/Projects/Karsio/2019-10-05_20-36-41.jpg" width="800" />
<img src="/assets/images/Projects/Karsio/2019-10-05_20-37-33.png" width="800" />
<img src="/assets/images/Projects/Karsio/2019-10-05_20-39-04.jpg" width="800" />
<img src="/assets/images/Projects/Karsio/2019-10-05_20-39-36.png" width="800" />
<img src="/assets/images/Projects/Karsio/2019-10-05_20-39-51.png" width="800" />
<img src="/assets/images/Projects/Karsio/2019-10-05_20-41-08.jpg" width="800" />
<img src="/assets/images/Projects/Karsio/2019-10-05_20-39-57.jpg" width="800" />
<img src="/assets/images/Projects/Karsio/2019-10-05_20-40-20.jpg" width="800" /> -->

## Rukiya's Concept Art:
<img src="/assets/images/Projects/Karsio/CarAmour.png" width="800" />
<img src="/assets/images/Projects/Karsio/Cars-2.png" width="800" />
<img src="/assets/images/Projects/Karsio/CarScene1.png" width="800" />
<img src="/assets/images/Projects/Karsio/CarScene2.png" width="800" />
<img src="/assets/images/Projects/Karsio/Tech.png" width="800" />
<img src="/assets/images/Projects/Karsio/Upgrades.png" width="800" />

--- 