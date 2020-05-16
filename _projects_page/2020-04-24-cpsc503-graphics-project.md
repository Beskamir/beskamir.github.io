---
layout: article
title: Computer Graphics Research Project
key: 20200424
permalink: /projects/graphics-research-project
cover: https://cdna.artstation.com/p/assets/images/images/026/720/716/large/sebastian-kopacz-lightingcompare.jpg?1589538133
aside:
  toc: true
article_header:
  type: cover
  image:
    src: https://cdnb.artstation.com/p/assets/images/images/026/720/735/large/sebastian-kopacz-neurons-2020-04-08-14-22-08.jpg?1589538060
---

Course project for the Project in Computer Graphics course (Computer Science 503.03 at the University of Calgary) I took in winter 2020 and where I upgraded the [RTX render engine I wrote last year](https://beskamir.github.io/projects/rendering-project) to support additional features such as ambient occlusion.

<!--more-->

[ArtStation Link](https://www.artstation.com/artwork/L2nRdk)

###### Source code is self-hosted on my home Git-Gogs server which is only accessible from my home network.

--- 
# Project Summary

## Objective

Apply my knowledge of Vulkan to improve neuron rendering in connectome visualizations with RTX ambient occlusion.

## Justification
- Opportunity to reuse last year's rendering project.
- Gain greater familiarity with RTX and the Vulkan API.
- Combination of computer graphics, art, and neuroscience.
- Improve existing connectome visualizations.

## Features
- Vulkan rasterizer with depth buffer.
- Ray tracer supports:
  - Direct Shadows.
  - Ambient Occlusion.
  - Diffuse Shading.
- Can switch between rasterizer and ray tracer rendering modes.
- User specified camera movement with the ability to disconnect the mouse to make screenshot taking easier.
- Uses assimp for quickly loading models with many polygons.
- Better/cleaner codebase than the previous version.
- Also supports model transformations using push constants. 
- Using a texture to encode the directions in which AO rays should be sent in.

## Challenges
- Various bugs such as accidentally destroying my acceleration structure buffer before it was finished copying and thus only being able to support about 5 thousand vertices... After resolving that bug, the ray tracer could easily support 50 million vertices.
- Learning more about the Vulkan API.
  - Push constants.
  - Depth buffer.
  - Not deleting the bottom level acceleration structure when it's still needed.
  - Passing textures to the ray tracing shaders.
  - etc.
- Creating a texture that encodes the directions in which rays should be sent for computing AO.
- Random vs Halton sequence for computing the directions in which AO rays should be sent. For some reason the Halton sequence created a repeating image texture so a random sequence was used instead.

## Final Report
[Here's a link to the final report I wrote for the course](\assets\images\Projects\NeuronAO\SebastianKopacz-FinalReport.pdf).

--- 

# Screenshots

## Final Neuron Visualization
<img src="https://cdnb.artstation.com/p/assets/images/images/026/720/735/large/sebastian-kopacz-neurons-2020-04-08-14-22-08.jpg?1589538060" width="100%" />
Neuron rendered with diffuse and ray traced ambient occlusion lighting.

## Shading Comparison
<img src="https://cdna.artstation.com/p/assets/images/images/026/720/716/large/sebastian-kopacz-lightingcompare.jpg?1589538133" width="100%" />
Comparison of the various shading modes my render engine supported.

## Render Engine Comparison
<img src="https://cdna.artstation.com/p/assets/images/images/026/720/724/large/sebastian-kopacz-enginecompare.jpg?1589538173" width="100%" />
Ambient occlusion comparison between my render engine (labeled Vulkan) and Blender's Cycles render engine (labeled Blender). My render engine was using fewer samples but otherwise I tried to match it as closely as possible.

## Effect of AO Ray Distance
<img src="https://cdna.artstation.com/p/assets/images/images/026/720/722/large/sebastian-kopacz-distancecompare.jpg?1589537986" width="100%" />
Comparison exploring the effect that ray distance has on ambient occlusion shading.

## AO Sampling
<img src="https://cdna.artstation.com/p/assets/images/images/026/720/720/large/sebastian-kopacz-samplecompare.jpg?1589537980" width="100%" />
<img src="https://cdna.artstation.com/p/assets/images/images/026/721/182/large/sebastian-kopacz-performance.jpg?1589539108" width="100%" />
The performance and visual impact of AO sampling without any denoising. As evident 32 samples is sufficient for a good enough effect at a high enough framerate on an RTX 2080.

## RTX Shadows
<img src="https://cdna.artstation.com/p/assets/images/images/026/721/680/large/sebastian-kopacz-neurons-2020-04-08-14-01-23.jpg?1589540449" width="100%" />
<img src="https://cdna.artstation.com/p/assets/images/images/026/721/682/large/sebastian-kopacz-neurons-2020-04-08-16-22-21.jpg?1589540453" width="100%" />
Unfortunately shadows detracted from neuron visualization. This is likely due to neuron's structure making shadows feel disconnected from the geometry casting them.

## AO Direction Textures
<img src="\assets\images\Projects\NeuronAO\SampleHemisphere.png" width="100%" />
<img src="\assets\images\Projects\NeuronAO\SampleTextures.png" width="100%" />
Due to time constraints I was unable to resolve why the Halton sequence resulted in an obviously repeating pattern. Instead I just used the image from the random sequence as it worked and time was a bit limited.

## Future Direction
<img src="https://cdnb.artstation.com/p/assets/images/images/026/720/729/large/sebastian-kopacz-6.jpg?1589538020" width="100%" />
The Fresnel node in Blender resulted in a nice effect that highlighted neuron edges really well and might improve neuron and therefore connectome visualizations.

# Videos

## Existing Connectome Rendering
<div style="position:relative;padding-top:56.25%;">
  <iframe src="https://www.youtube.com/embed/PeyHKdmBpqY"  frameborder="0" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;"></iframe>
</div>

## My Neuron Rendering
<div style="position:relative;padding-top:56.25%;">
  <iframe src="https://www.youtube.com/embed/1qnOz-2JF64"  frameborder="0" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;"></iframe>
</div>

---

# Credits
## Vulkan Resources
- [Alexander Overvoorde's Vulkan-Tutorial](https://vulkan-tutorial.com/).
- [Sascha Willems's Vulkan Examples and Demos](https://github.com/SaschaWillems/Vulkan).
- [Vulkan API and Documentation](https://vulkan.lunarg.com/doc/view/latest/windows/apispec.html).

## RTX Resources
- [Martin-Karl Lefrançois and Pascal Gautron's Vulkan RTX Tutorial on Nvidia's blog](https://developer.nvidia.com/rtx/raytracing/vkray).
- [Sergii Kudlai's Vulkan RTX Tutorial](https://iorange.github.io/p01/HappyTriangle.html).
- [Ambient occlusion based on Jakub Boksansky's RTAO project](https://github.com/boksajak/RTAO).

## Neuron Dataset
- [Neuron data from the Hemibrain connectome project](https://www.janelia.org/project-team/flyem/hemibrain).
- [Neurons converted to OBJ files using the SWC Mesher Blender addon](https://github.com/mcellteam/swc_mesher).

## General Credits
- [The event system, logger, and window startup are all based on early versions of Yan Chernikov's Hazel game engine since that was what the previous version of this project was based on](https://github.com/TheCherno/Hazel).

---