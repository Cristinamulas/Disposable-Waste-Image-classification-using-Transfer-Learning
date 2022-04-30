

<a href="http://www.youtube.com/watch?feature=player_embedded&v=s5kUSMUaZLM" target="_blank"><img src="http://img.youtube.com/vi/s5kUSMUaZLM/0.jpg"
alt="Rob Lanphier: Editing Wikipedia: Because Someone Has to..." width="50%" /></a>



# Image classification Using Transfer Learning 


## Goal
The motivation of this project is to build an image classifier capable of predicting disposable waste images into six different categories: cardboard, glass, metal, paper, plastic and trash.

## Introduction

This study aimed to build image classifiers in the domain of disposable waste images. With this project, I want to understand how to solve an image classification problem through using Transfer Learning. Transfer Learning is usually used in computer vision tasks where only a small amount of data is available. In this project, I’m going to implement a VGG16 model which is a pre-trained network. This model was pre-trained on the ImageNet dataset. I’m going to use this pre-trained architecture as a base model. Then, I will remove the fully connected layers and try different networks to classificate the images into six categories.

## Problem Description

In the days that we are living, climate change is a significant problem and it can get worse over time if we don't take the right action. Nowadays, recycling can help tackle the climate change crisis, because when we recycle we can save energy and it can also reduce greenhouse gas emission. Sometimes garbage is incorrectly disposed and this can lead to recycling contamination. This type of contamination is a huge problem in the recycling industry because it can increase the cost to process recyclables. This is why building an image classifier to classify waste disposal is important. 

## Dataset
The dataset is from this Github [repo](https://github.com/garythung/trashnet) consists of 2,527 images, divided into 6 different categories: 

- 501 images of glass
- 594 images of  paper
- 403 images of cardboard
- 482 images of plastic
- 410 images of metal
- 137 images of trash

## Models

In this project, I implemented a pre-trained network: VGG16 as a base mode. In addition, I wanted to test how many fully connected layers the base model needed to give the best results. So I implemented different models with different numbers of FC layers. First, I started with one fully connected layer with 128 neurons with ReLu as activation function and a output layer with six neurons with softmax as an activation function. For the second model, I added another FC layer to the base model, so the architecture of this model is two FC layers with ReLu function and a output layer with 6 neurons and softmax activation function. The third model architecture contains two fully connected layers with ReLu as activation function and a dropout layer for regularization purposes and an output layer with six neurons and a softmax activation function. 

For calculating the loss, I used a categorical cross entropy function. I used Adam optimizer with a learning rate of 0.005 and I also tried RMSprop optimizer. To evaluate my results, the metrics that I used were: accuracy, precions, recall, F1 score and confusion matrix for each of my networks.

## Results


The model with two dense FC layers and the dropout layers, trained with 100 epochs and a batch size of 100 with RMSprop optimizer gives the best results with a validation accuracy of 68.0%.



<img src=https://github.com/Cristinamulas/Disposable-Waste-Image-classification-using-Transfer-Learning/blob/main/images/Screen%20Shot%202020-12-03%20at%204.48.39%20PM.png width="480">


<img src=https://github.com/Cristinamulas/Disposable-Waste-Image-classification-using-Transfer-Learning/blob/main/images/Screen%20Shot%202020-12-08%20at%2012.09.17%20PM.png width="380">


<img src=https://github.com/Cristinamulas/Disposable-Waste-Image-classification-using-Transfer-Learning/blob/main/images/Screen%20Shot%202020-12-08%20at%2012.16.19%20PM.png width="380">

## Conclusion/Future Work


In this study, I presented results using Transfer Learning to classificate waste disposal images. I confidently identified which was the best network that can successfully predict the class of the image. 

In future work, it will be interesting to collect more images and add a non-trash class. In addition, I would like to implement other pre-trained networks like for example Resnet-50, and compare the results between both models.



