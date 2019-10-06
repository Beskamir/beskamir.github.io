---
layout: article
title: Karsio Engine and Game
key: 20180320
permalink: /projects/Karsio
cover: /assets/images/Projects/Karsio/2019-10-05_23-11-04.png
aside:
  toc: true
article_header:
  type: cover
  image:
    src: /assets/images/Projects/Karsio/2019-10-05_23-11-04.png
---

Group course project for the _Games Programming_ course (Computer Science 585 at the University of Calgary) I took in winter 2018 and where I worked in a team of 4 (Ben, Rukiya, Brian, and myself) to build a game engine and of course the game itself.

<!--more-->

<!-- ##### Links to additional images on my ArtStation:
- [Test for BVH vs KD trees in PBRT](https://www.artstation.com/artwork/N5gAaP)
- [Polygonal apertures in PBRT](https://www.artstation.com/artwork/A960v5)
- [Deferred rendering in OpenGL](https://www.artstation.com/artwork/nQvA2X)
- [SSAO in OpenGL](https://www.artstation.com/artwork/RYgAXy) -->

[Link to source code](https://github.com/Beskamir/KarsioVS)

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
  - Chassis
    - Unlocks higher level upgrades but makes you larger and slows you down.
  - Weapon
    - More damage or faster firing rate depending on upgrade.
  - Armor
    - Take less damage when hit.
  - Ram
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
- As usual, [LearnOpenGL](https://learnopengl.com/) helped me figure out how to use OpenGL.
- Space skybox generated using [Spacescape](http://alexcpeterson.com/spacescape/).

---

# Ingame Footage:

## Video:

<iframe width="560" height="315" src="https://www.youtube.com/embed/cg6CkGn4yRI" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
For some reason audio wasn't recorded (and it may be copyrighted anyway) so for the full effect, get the game on GitHub and compile it yourself.

## Screenshots: 
<img src="/assets/images/Projects/Karsio/2019-10-05_23-11-04.png" width="800" />
<img src="/assets/images/Projects/Karsio/2019-10-05_20-36-31.png" width="800" />
<img src="/assets/images/Projects/Karsio/2019-10-05_20-36-41.jpg" width="800" />
<img src="/assets/images/Projects/Karsio/2019-10-05_20-37-33.png" width="800" />
<img src="/assets/images/Projects/Karsio/2019-10-05_20-39-04.jpg" width="800" />
<img src="/assets/images/Projects/Karsio/2019-10-05_20-39-36.png" width="800" />
<img src="/assets/images/Projects/Karsio/2019-10-05_20-39-51.png" width="800" />
<img src="/assets/images/Projects/Karsio/2019-10-05_20-41-08.jpg" width="800" />
<img src="/assets/images/Projects/Karsio/2019-10-05_20-39-57.jpg" width="800" />
<img src="/assets/images/Projects/Karsio/2019-10-05_20-40-20.jpg" width="800" />

