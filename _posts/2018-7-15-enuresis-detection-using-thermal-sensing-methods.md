---
title: Enuresis Detection Using Thermal Sensing Methods
date: 2018-7-15
comment: false
---
This is my undergraduate research project: to develop a bed-based toolset to monitor a disabled child’s health and activity during the night. My role in this project is to design an anutomate system using thermal sensing methods (theromocouple and digital temperature sensor) for enuresis detection.


## Workflow
1. preprocessing: 3D cardiac images are sliced into individual 2D images and cropped to 128*128.
2. modified 2d U-Net architecture: adding a batch normalization layer and a dropout layer to prevent overfitting.
3. 2D U-Net segmentation: properly train the 2D U-Net and use it to take the input MRI image and perform segmentation.
4. post-processing via morphological opening a d closing: remove small structures and fill any holes.
5. pathology classification using random forest: 15 features are selected for classification and the classifier contains contains 5 classes (normal, HCM, DCM, MINF, RVA).

<p align="center">
  <img src="https://github.com/shangxwang/shangxwang.github.io/blob/master/github/cardiac.png?raw=true">
</p>

