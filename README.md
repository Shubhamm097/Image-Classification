# Image Classification: Intel Image Kaggle Competition

## Table of Contents
  * [Overview](#overview)
  * [Motivation](#motivation)
  * [Approach](#approach)
  * [Run](#run)
  * [Bug / Feature Request](#bug---feature-request)
  * [Technology Stack](#technology-stack)
  * [Credits](#credits)


## Overview
The project can be treated as a guide for a simple imagle classification tasks using a basic CNN architecture and by transfer learning using ResNet50 architecture. The model is able to classify the image as buildings, mountain, glacier, sea, street and forest. This is also part of [Kaggle Datasets](https://www.kaggle.com/puneet6060/intel-image-classification).

## Motivation
It is difficult for one to fine-tune the results, however, fine-tuning can be done but if you are running late then transfer learning can help you catch up with that without compromising the results. Thus, it is important for one to know the options that one has while developing a project using transfer learning.

## Approach
At first, the images are transformed in order to match the number of input features of the image with the required model that you have chosen.

Now, initially I tried building up a basic CNN architecture by myself with a bunch of layers having convolution layer, alongside regularization and ReLU activation function, having max-pooling after the convolution layer. It gave around 72-73% accuracy.

Thus, in order to increase the accuracy by a reasonable amount, transfer learnong can be used. There are a lot of pre-built models like mobilenet, GoogleNet, InceptionNet that can be used to classify the image. I have used ResNet50 here. I froze the layers of ResNet50 and added a couple of dense layers alongside and regularization layer and then trained the dataset over the added layers. It gave an accuracy of approx 91%. There are a couple of ways a model can be trained while using a pre-built models.

1. One can train the pre-built model from the start over their own respective dataset, this could take some time depending upon the size of the model and the datset.

2. The other way, could be to freeze the layers of the pre-trained model and add your own layers and train the dataset over those layers, this will take less time comparatively.


## Run
After downloading the dataset from [here](https://www.kaggle.com/puneet6060/intel-image-classification), open a google colab notebook and run the cells.


## Bug / Feature Request
If you'd like to request a new feature/approach, feel free to do so by opening an issue [here](https://github.com/Shubhamm097/Image-Classification/issues/new). Please include the relevant reasons for the feature or approach.

## Technology Stack
1. PyTorch
2. Python
3. ResNet50 Architecture
4. Keras
5. Convolutional Neural Networks


## Credits
- [Understand ResNet50 Architecture](https://towardsdatascience.com/understanding-and-coding-a-resnet-in-keras-446d7ff84d33)

- [Kaggle Dataset for Image Classification](https://www.kaggle.com/puneet6060/intel-image-classification)

- [Understand Convolutional Networks](https://towardsdatascience.com/a-comprehensive-guide-to-convolutional-neural-networks-the-eli5-way-3bd2b1164a53)
