---
layout: article
title: Blender Simplicity 2018 Challenge
key: 20180920
permalink: /projects/simplicity-2018
cover: https://cdna.artstation.com/p/assets/images/images/012/809/418/large/sebastian-kopacz-fractal01-composited.jpg?1536640185
aside:
  toc: true
article_header:
  type: cover
  image:
    src: https://cdnb.artstation.com/p/assets/images/images/012/809/703/large/sebastian-kopacz-marchingcubesfinal.jpg?1536640168
---

Collection of entries for Remington's 2018 simplicity challenge where the objective was to create some cool artwork while only using a limited amount of Blender's features. 

<!--more-->


##### Links to additional images on my ArtStation
- [T-Cube fractal](https://www.artstation.com/artwork/9ve8N)
- [DNA strand](https://www.artstation.com/artwork/3RoE2)
- [Implicit heart model](https://www.artstation.com/artwork/vN1zx)
- [Implicit models in a scene](https://www.artstation.com/artwork/5m8dW)

###### Source code is self-hosted on my home Git-Gogs server which is only accessible from my home network.

# Justification

Grant Wilk from Remington Graphics (now Remington Creative), hosted a Blender competition where one of the challenges was to create a model using just Blender's object mode. As such modifying individual vertices was generally against the rules unless it was done through applying transformations within object mode. Despite overlooking that it was supposed to be just a single model and not a complete scene it was still really enjoyable since 3 of my entries gave me a reason to figure out Blender's API for scripting UI inputs.

---

# Fractal

## T-Cube

### Features
- Simple recursive implementation of a T-Cube fractal.
   - Placed cubes recursively until a certain depth was reached.
   - Made as a simple test of Blender's scripting API.
- Added a nice procedural material to the resulting cubes.

### Result
<img src="https://cdna.artstation.com/p/assets/images/images/012/809/418/large/sebastian-kopacz-fractal01-composited.jpg?1536640185" width="800" />

### Credits
- Blender's API documentation. 

---
# DNA Strand

### Features
- Considered making a script but ended up making it manually by hand.
- Mostly a compositing project. (It was saved in post)

### Before compositing 
<img src="https://cdna.artstation.com/p/assets/images/images/012/809/562/large/sebastian-kopacz-dna-raw.jpg?1536638347" width="800" />

### After compositing
<img src="https://cdna.artstation.com/p/assets/images/images/021/202/910/large/sebastian-kopacz-dna-composited.jpg?1570760857" width="800" />

### Credits
- Blender's API documentation. 

---

# Implicit Surfaces

## Heart 

### Features
- Places voxels based on an implicit surface.
- Voxels can both be normal cubes and custom made cubes that were manually created using object mode and emulate marching cubes.

### Result: 
<img src="https://cdnb.artstation.com/p/assets/images/images/012/809/703/large/sebastian-kopacz-marchingcubesfinal.jpg?1536640168" width="800" />

### Credits:
- Blender's API documentation. 
- Heart implicit surface equation from the [second assignment](http://beskamir.github.io/projects/haptics-assignments#implicit-surfaces) of the *Computer Haptics* course (Computer Science 599.86 at the University of Calgary) I took in winter 2018.

## Scene

### Features
- Most of the scene built using my implicit surface voxelizer
  
### Result
<img src="https://cdna.artstation.com/p/assets/images/images/012/809/820/large/sebastian-kopacz-implicitscene.jpg?1536640128" width="800" />

### Credits
- Blender's API documentation
- Most of the implicit surface equations used in this scene are from [Implicit Algebraic Surfaces](https://www-sop.inria.fr/galaad/surface/)
- Some implicit surfaces equations from the [second assignment](http://beskamir.github.io/projects/haptics-assignments#implicit-surfaces) of the *Computer Haptics* course (Computer Science 599.86 at the University of Calgary) I took in winter 2018.
- Remaining models made in blender using object mode as per the competition's rules.

---
