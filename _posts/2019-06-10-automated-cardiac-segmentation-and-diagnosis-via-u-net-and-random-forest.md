---
title: Automated Cardiac Segmentation and Diagnosis via U-Net and Random Forest
date: 2019-06-10
comment: false
---
In this project, we automate cardiac MRI image segmentation and disease diagnosis through deep network and machine learning techniques on 3D cine-MR images. U-Net is implemented to segment the left ventricle (LV), right ventricle (RV), and myocardium (MYO). Features extracted from the U-Net segmentation result and the original MRI image are then fed into a random forest classifier to diagnose if the patient has myocardial infarction (MINF), dilated cardiomyopathy (DCM), hypertrophic cardiomyopathy (HCM), abnormal right ventricle (RV), or no cardiac disease. 


## Workflow
1. preprocessing: 3D cardiac images are sliced into individual 2D images and cropped to 128*128.
2. modified 2d U-Net architecture: adding a batch normalization layer and a dropout layer to prevent overfitting.
3. training the network.
4. 2D U-Net segmentation: use a 2D U-Net that takes as input the MRI image to perform segmentation.
5. post-processing via morphological opening a d closing: remove small structures and fill any holes.
6. pathology classification using random forest: 15 features are selected for classification and the classifier contains contains 5 classes (normal, HCM, DCM, MINF, RVA).

<p align="center">
  <img src="https://github.com/shangxwang/shangxwang.github.io/blob/master/github/cardiac.png?raw=true">
</p>

## Results
The network is able to produce a mean dice coefficient of 0.82, while the classification accuracy is 0.76 since it depends on the segmentation result. 
