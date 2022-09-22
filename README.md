# Object_Detection_For_Faces
Build a Face Detection model 


## Objective of this notebook
- The purpose of this notebook is to build a Face Detection model 
- Details of the **problem statement**  , **data set** ,  **summary of the code/solution**  , **sample output/Prediction** from the program and **final result** of the project are listed in the sections to follow.

## Problem Statement 
Computer Vision can be used to detect faces which is useful in multiple domains.In this particular use case , a company wants to automate the process of cast and crew information in each scene from a movie such that when a user pauses on the movie and clicks on cast information button, the app will show details of the actor in the scene.


## Data Description:
The dataset comprises of images and its mask where there is a human face

## Domain:
  Entertainment

## Summary of the Solution/Code:
The code aims at building a face detection model with an additional requirement of displaying the the face object with a mask.
- We begin by doing an Exploratory Data analyses and Visualisation/viewing of the images 
- We then do the required pre-processing for the data to make it compatible with the model to be built.
- We have been given only the bounding box as labels in training data ,masked images for/as labels have not been given.Since we have been specifically asked to create   face masks , we will be using the bounding box it self as the mask and treat this problem as a sematic segmentation problem.
- We will use an algorithm that does semantic segmentation to model the same .We will be using Mask-RCNN.
- We build the model using a reliable third part implementation of Mask-RCNN(Mask R-CNN Project developed by Matterport) which has been built on top of the Keras deep learning framework
- Essentialy , what we do in the code is load a pre-trained Mask-RCNN model , omit the top layers . 
- We then re-train the model with "faces" data & tune to get the best results/minimum loss
- Finally we evaluate our model on Test data with the chosen metric as mAp.
- Refer **python worksheet  Project_P1_FaceMaskDetection.ipynb** for the solution

## Sample Ouput/Prediction :
Here is a sample result/output from the program/model 

![image](https://user-images.githubusercontent.com/68383273/191735599-d115c8f4-ccf3-4458-bf31-95b052ef4262.png)
![image](https://user-images.githubusercontent.com/68383273/191736008-b66da155-c404-499c-ab10-bd1cf2860f35.png)


## Result
- We have obtained a .80 MAP on Train Set & a 0.681 on Test Set
- Further training of model would have given us better results 
- This can be considered as an extesion to improec the performace of this model
