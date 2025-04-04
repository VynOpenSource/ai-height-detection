# ai-height-detection

## Table of contents

- [Introduction](#introduction)
- [Pipeline](#pipeline)
- [Dataset](#dataset)
- [Steps to use project](#steps-to-use-project)
- [Results](#results)
- [Output](#output)
- [Dataset References](#dataset-references)
- [Contributors](#contributors)

## Introduction

Working at height is one of the biggest cause of fatalities and major injuries. It includes falls from high raised platforms, ladders or through fragile surfaces.

So we have trained a deep learning model to detect if a person is working at a height in given image. Technique used is fine tuning of Resnet50 architecture. Image Augmentation was used to increase Dataset. Frame work used is Tensorflow.

## Pipeline
![Pipeline](https://github.com/VynOpenSource/HeightDetection/blob/main/src/readmeImages/pipe.png)

## Dataset 

Dataset includes thousands of positive, negative and hard examples for the person working at height, collected from open sources.
This dataset is saved in drive, can be accessed from here: [positive](https://vyn-opensource-ai-datasets.s3-eu-west-1.amazonaws.com/ai-height-detection/training-data/train_positive.zip), [negative](https://vyn-opensource-ai-datasets.s3-eu-west-1.amazonaws.com/ai-height-detection/training-data/train_negative.zip), [hard](https://vyn-opensource-ai-datasets.s3-eu-west-1.amazonaws.com/ai-height-detection/training-data/train_hard.zip).

Some of the links from which images have been downloaded, are listed in [Dataset References](#dataset-references).

## Steps to use project


##### Step1: Clone this folder to you local PC.
(If in windows, also install MingW for 'make' commands.)

##### Step2: Open command prompt, run "pip install -r requirements.txt"

##### Step3: Now for to download already trained models. 

- Run "make getModel2" for 2 class model in directory ./models.
- Run "make getModel3" for 3 class model in directory ./models.

##### Step4: To test these models:

- Insert images in testingImages folder, which you want to test.
- Then run "make test2" for 2 class model results.
- Or run "make test3" for 3 class model results.

##### Step5: To download dataset:

- Run "make getData2" to get data for 2 class model in directory ./data/data2.
- Run "make getData3" to get data for 3 class model in directory ./data/data3.

##### Step6: To train again, after downloading dataset:

- Run "make train2" and your new model2 will be saved in modelNew directory.
- Run "make train3" and your neew model3 will be saved in modelNew directory.

## Results

***Two class Model***-> Training Accuracy: **94%** , Testing Accuracy: **91%** (Height, Not Height)

***Three class Model***-> Training Accuracy: **83%** , Testing Accuracy: **72%** (Height, Not Height, Hard)


## Output
<img src="https://github.com/VynOpenSource/HeightDetection/blob/main/testingImages/imagen1.jpg" width="400" height="250">

Not height, Probability [8.759406e-11]


<img src="https://github.com/VynOpenSource/HeightDetection/blob/main/testingImages/imagen2.jpg" width="400" height="250">

Not height, Probability [2.0659362e-20]


<img src="https://github.com/VynOpenSource/HeightDetection/blob/main/testingImages/imagep1.jpg" width="400" height="250">

Height, Probability [0.99990416]


<img src="https://github.com/VynOpenSource/HeightDetection/blob/main/testingImages/imagep2.jpg" width="400" height="250">

Height, Probability [0.99976885]

## Dataset References
All source images were picked from sources where the license allowed permissible use for commercial purposes. Some of the sources used were the following: 
- Unsplash
- Pixabay
- Free Nature Stock
- Realistic Shots
- Life of pix
- Gratisography
- StockSnap

## Contributors
This project was undertaken under the
under the leadership of Professor Brejesh (IITD) and the Data Science team at vyntelligence.

### Code Contributors
[Sourav Kumar](https://github.com/souravk1113)   
[Amenreet Singh Sodhi](https://github.com/scaryGangsta)   
[Manav Bansal](https://github.com/ManavBansal)  

