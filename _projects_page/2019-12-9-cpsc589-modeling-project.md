---
layout: article
title: Computer Graphics Modeling Project
key: 20191209
permalink: /projects/modeling-project
cover: assets\images\Projects\Modeling\5.png
aside:
  toc: true
article_header:
  type: cover
  image:
    src: assets\images\Projects\Modeling\BunnyCompare.png
---

Group course project for the modeling course (Computer Science 589 at the University of Calgary) I took in fall 2019 and where we (Chris, Cassandra, and myself) wrote a Blender addon that created 3D models from six orthogonal depth maps. 

<!--more-->

##### [Links to source code](https://github.com/Beskamir/BlenderDepthMaps)

---

# Project Summary

## Objective

- Create models using six orthogonal depth maps.
- Provide some user interface for doing this from within Blender.

## Features
- Output consisted of:
  - Point cloud
  - Voxels
  - Marching cube reconstructed surface
- Automated mesh cleanup to remove outlining data.
- Reasonable user interface allowed for generating models from within Blender.
- Supported generated and manually drawn depth maps.

## My Focus

### Geometry Reconstructions
- Placed voxels based on data extracted from the depth maps.
- Used marching cubes for surface reconstruction.

### Depth Maps
- Authoring good test depth maps.
- Focus was on creating or finding models that when converted into depth maps would be good tests for edge cases.
- Later found and converted common 3D test models into depth maps.

### Credits
- My excellent team members Chris and Cassandra.
- [Blender API documentation](https://docs.blender.org/api/current/index.html).
- Test models obtained from the [list of common 3D test models](https://en.wikipedia.org/wiki/List_of_common_3D_test_models).

---

# Screenshots 

## Stanford Bunny
<img src="\assets\images\Projects\Modeling\BunnyCompare.png" width="100%" />
Left image uses marching cube surface reconstruction, right image uses voxels. 

<img src="\assets\images\Projects\Modeling\PointMarching.png" width="100%" />
Marching cubes overlaid with point cloud.

## Stanford Dragon
<img src="\assets\images\Projects\Modeling\DragonMessy.png" width="100%" />
Reconstruction sometimes results in noise as evident in the right images.

<img src="\assets\images\Projects\Modeling\DragonCleanup.png" width="100%" />
That noise sometimes results in non-manifold lines as evident in the left and middle images. Fortunately Chris figured out how to automatically remove these from the mesh allowing for an automated mesh cleanup.

<img src="\assets\images\Projects\Modeling\Dragon.png" width="100%" />
Left image is reconstructed using marching cubes with automated cleanup while the right image uses voxels with automated cleanup.


## Extra Images
<img src="\assets\images\Projects\Modeling\1.png" width="100%" />
<img src="\assets\images\Projects\Modeling\2.png" width="100%" />
<img src="\assets\images\Projects\Modeling\3.png" width="100%" />
<img src="\assets\images\Projects\Modeling\4.png" width="100%" />
<img src="\assets\images\Projects\Modeling\5.png" width="100%" />
<img src="\assets\images\Projects\Modeling\6.png" width="100%" />
<img src="\assets\images\Projects\Modeling\7.png" width="100%" />

--- 