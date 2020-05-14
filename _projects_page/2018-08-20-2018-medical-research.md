---
layout: article
title: Summer Research
key: 20180920
permalink: /projects/medical-2018
aside:
  toc: true
---

Used machine learning to automatically landmark 3D face scans for medical purposes.

<!--more-->

---

# Justification

- Thousands of unlabeled 3D scanned faces.
- I wanted to gain a better understanding of how to use machine learning.
- My task was to train a neural network to label them with appropriate landmarks.

---

# Pipeline

- Used the Visualization Toolkit (VTK) to create pipeline for rendering models with multi-camera setups.
- Multi-camera setup was based on a mesh defined in an obj file so it was easily modifiable.
- Trained a Convolutional Neural Network on the rendered images using the Keras neural network API.

---

# Learned

- Machine learning using Keras. 
- VTK rendering with multiple camera positions.
- Working in the Medical Image Processing and Machine Learning Laboratory at the University of Calgary.


--- 

# Challenges

- Training neural networks is computationally intensive (especially when you don't fully know what you're doing yet).
- I enjoyed the engineering part too much while somewhat neglecting the scientific components (end result) of the project.


---
