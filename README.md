# Image classification Using Transfer Learning 

## Goal
The motivation of this project is to build an image classifier capable of predicting disposable waste images into six different categories: cardboard, glass, metal, paper, plastic and trash.


## Introduction

This study aimed to build image classifiers in the domain of disposable waste images. With this project, I want to understand how to solve an image classification problem through using Transfer Learning. Transfer Learning is usually used in computer vision tasks where only a small amount of data is available. In this project, I’m going to implement a VGG16 model which is a pre-trained network. This model was pre-trained on the ImageNet dataset. I’m going to use this pre-trained architecture as a base model. Then, I will remove the fully connected layers and try different networks to classificate the images into six categories.

## Problem Description

In the days that we are living, climate change is a significant problem and it can get worse over time if we don't take the right action. Nowadays, recycling can help tackle the climate change crisis, because when we recycle we can save energy and it can also reduce greenhouse gas emission. Sometimes garbage is incorrectly disposed and this can lead to recycling contamination. This type of contamination is a huge problem in the recycling industry because it can increase the cost to process recyclables. This is why building an image classifier to classify waste disposal is important. 

## Dataset
The dataset is from this Github repo [repo](https://github.com/garythung/trashnet) consists of 2,527 images, divided into 6 different categories: 

- 501 images of glass
- 594 images of  paper
- 403 images of cardboard
- 482 images of plastic
- 410 images of metal
- 137 images of trash

