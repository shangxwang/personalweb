---
title: Thalamus Segmentation via Deep Learning
date: 2020-09-20
comment: false
---

Segmenting the thalamus using a 3D convolutional neural network that takes the MPRAGE image and a set of features derived from diffusion tensor images (DTI). 
<p align="center">
  <img src="https://github.com/shangxwang/shangxwang.github.io/blob/master/github/thalamus_workflow.png?raw=true">
</p>


## Workflow
1. preprocessing:All the images are registered to MNI space and N4 corrected.
2. constructing a thalamus locating box: 
We learn the location of the thalamus from 234 images that have been processed by MACRUISE12 whole brain segmentation. The bounding box is found through binarizing the probability map and finding the minimum and maximum locations of the mask on each axis (x,y,z); which we then enlarge to cover reasonable natural variation.
3. 3D U-Net segmentation: use a 3D U-Net that takes as input the MPRAGE image and a set of features derived from DTI to perform segmentation.
4. post-processing: retain only the largest connected component and fill any holes within the largest connected component.

<p align="center">
  <img src="https://github.com/shangxwang/shangxwang.github.io/blob/master/github/thalamus_workflow.png?raw=true">
</p>

## Results
Our proposed framework is able to produce a mean dice coefficient of 0.842, comparing to the state-of-art's 0.816 dice coefficient.



