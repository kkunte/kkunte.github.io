---
layout: post
title:  "My implementation of ResNet model"
date:   2019-11-09 00:05:06 -0500
categories: Machine Learning 
---



The ["Deep Residual Learning for Image Recognition"](https://arxiv.org/pdf/1512.03385.pdf) paper was published in 2015 and it won that year's ImageNet classification competition by a significant margin.
It introduced a new Neural Net architecture called "Residual Network" or ResNet as they are popularly known since then.

The idea is simple and elegant and it solved the problem of propagating gradient information that is absolutely crucial for training deep networks. 

Today, ResNets and their variants form the backbone of more sophisticated networks used for object detection, classification and other computer vision tasks. Learning to implement and train a ResNet model is crucial skill to acquire before trying to tackle more complicated things.

I studied implementations such as <https://github.com/kuangliu/pytorch-cifar/tree/master/models> , <https://github.com/akamaster/pytorch_resnet_cifar10> and then decided to create my own version.


I made few mistakes along the way which prevented the model from reaching the level of accuracy mentioned in the paper.
1. Forgot to add Relu Activation after the first convolutional layer..Duh !
2. I applied the data augmentation transforms such as random horizontal flip and crop  to the test images as well by mistake.
3. I reduced the learning rate during training way too early. 

You can find my implementation [here](https://github.com/kkunte/computer_vision/blob/master/ResNet_CIFAR10.ipynb)

