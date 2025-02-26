---
layout: article
title: OpenGL Rendering and Raytracing
key: 20171127
permalink: /projects/intro-to-graphics
cover: https://cdna.artstation.com/p/assets/images/images/014/259/400/large/sebastian-kopacz-custom.jpg?1543234486
aside:
  toc: true
article_header:
  type: cover
  image:
    src: https://cdnb.artstation.com/p/assets/images/images/014/257/445/large/sebastian-kopacz-chessboard02.jpg?1543227840
---

Collection of the 4 assignments I completed for the Intro to Computer Graphics course (Computer Science 453 at the University of Calgary) I took in fall 2017.

<!--more-->

##### Links to additional pictures on my ArtStation
- [Hilbert curve in OpenGL](https://www.artstation.com/artwork/0X3kOV)
- [Image manipulation in OpenGL](https://www.artstation.com/artwork/oO2m2z)
- [Basic 3D model viewer in OpenGL](https://www.artstation.com/artwork/Vdy9P5)
- [Whitted ray tracer](https://www.artstation.com/artwork/nQEy0X)

##### [Source code](https://github.com/Beskamir/Intro-to-Computer-Graphics)

---
# Hilbert Curve  

## Features
- Rendering done with OpenGL.
- Draws first to tenth order Hilbert Curves using OpenGL's lines as well as by using thin triangles.

### 7th order Hilbert Curve
<img src="https://cdnb.artstation.com/p/assets/images/images/014/276/469/large/sebastian-kopacz-assignment1-2018-11-26-23-06-56.jpg?1543298910" width="100%" />

## Credits
- Regarding the software implementation the following resources were invaluable: 
   - [LearnOpenGL](https://learnopengl.com) for figuring out OpenGL. 
   - [GLFW documentation](https://www.glfw.org/docs/latest/) for figuring out the window and input.

---
# Image Manipulation  

## Features
- Rendering done with OpenGL.
- Draw multi-colored Catmull-Rom curves and loops.
- Apply image filters (grayscale and 2-bit quantization).
- Grayscale filter uses NTSC conversion weights.
- Move and scale the image.


### All effects active
<img src="https://cdnb.artstation.com/p/assets/images/images/014/257/939/large/sebastian-kopacz-bonusimage.jpg?1543232178" width="100%"  />

### Original image
<img src="https://cdnb.artstation.com/p/assets/images/images/014/258/571/large/sebastian-kopacz-tower.jpg?1543231507" width="100%"  />

### Grayscale
<img src="https://cdnb.artstation.com/p/assets/images/images/014/258/845/large/sebastian-kopacz-greyscale.jpg?1543232531" width="100%"  />

### 2-bit image quantization
<img src="https://cdnb.artstation.com/p/assets/images/images/014/276/275/large/sebastian-kopacz-2bit.jpg?1543297907" width="100%"  />


## Credits
- Original image is by realdreadstar/Natty Dread and he made it by setting up a custom scene in The Witcher 3 and taking a screenshot of it.
    - [Link to realdreadstar's version on the Nexus](https://www.nexusmods.com/witcher3/images/1239)
    - [Link to Natty Dread's version on Flickr](https://www.flickr.com/photos/90866390@N06/17649150394/in/dateposted-public/)
  - Regarding the software implementation the following resources were invaluable: 
   - [LearnOpenGL](https://learnopengl.com) for figuring out OpenGL. 
   - [GLFW documentation](https://www.glfw.org/docs/latest/) for figuring out the window and input.
   - Lines drawn using [Victoria Rudakova's tutorial](https://vicrucann.github.io/tutorials/osg-shader-3dlines/).

---
# Model Viewer and Editor


## Features
- Rendering done with OpenGL.
- Models can be selected by mouse clicking on them.
- Selected models can be modified by rotating, scaling, translating, duplicating, or turning various textures on or off.
  - Powerful enough to build the demo scene by hand.
- Supports basic OBJ features and models/textures can be imported with a config file or command-line arguments.
- Phong lighting model using diffuse, specular and ambient occlusion textures.
  
### Scene demoing model viewer
<div id="image-table">
    <table>
	    <tr>
    	    <td style="padding:1px">
        	    <img src="https://cdnb.artstation.com/p/assets/images/images/014/257/445/large/sebastian-kopacz-chessboard02.jpg?1543227840"  width="100%" />
      	    </td>
            <td style="padding:1px">
            	<img src="https://cdna.artstation.com/p/assets/images/images/014/257/446/large/sebastian-kopacz-chessboard.jpg?1543226413" width="100%" />
             </td>
        </tr>
    </table>
</div>
 
   
## Credits
- All models and textures shown in the image were provided to us by the TA as part of the course.
- Regarding the software implementation the following resources were invaluable: 
   - [LearnOpenGL](https://learnopengl.com) for figuring out OpenGL. 
   - [GLFW documentation](https://www.glfw.org/docs/latest/) for figuring out the window and input.
   - [Object selection](https://en.wikibooks.org/wiki/OpenGL_Programming/Object_selection) for figuring out how select objects by clicking on them.

---
# Whitted Ray Tracer
  
## Features
- CPU only and thus does not make use of OpenGL in any way.
- Ray intersection test for spheres and triangles.
- Functional shadow, reflection, refraction, and diffuse bounces.
- Gamma correction.
- Procedural textures.
- Directional and point lights.
- Supports basic OBJ features and models can be loaded with a config file.
  
### My custom scene
<img src="https://cdna.artstation.com/p/assets/images/images/014/259/400/large/sebastian-kopacz-custom.jpg?1543234486" width="100%" />

### Default Cornell box
<img src="https://cdnb.artstation.com/p/assets/images/images/014/259/407/large/sebastian-kopacz-default.jpg?1543234451" width="100%" />

## Credits
- All models either made by me or specified in the assignment description.
- Most of the ray tracer code was based on [Scratchapixel](https://www.scratchapixel.com/).

---
