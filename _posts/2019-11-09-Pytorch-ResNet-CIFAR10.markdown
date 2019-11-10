---
layout: post
title:  "Implementation of ResNet model in Pytorch"
date:   2019-11-09 00:05:06 -0500
categories: Machine Learning 
---



The ["Deep Residual Learning for Image Recognition"](https://arxiv.org/pdf/1512.03385.pdf) paper was published in 2015. It introduced a new Neural Net architecture called "Residual Network" or ResNet as it is popularly known since then. ResNet model won that year's ImageNet classification competition by a significant margin.

The idea of Residual Network module is elegant and it solves the problem of efficently propagating gradient information through all layers of deep networks. This ability is critical for successfully training a deep neural network.

Today, ResNets and their variants form the backbone of more sophisticated networks used for object detection, classification and other computer vision tasks. Learning to implement and train a ResNet model is thus a crucial skill to acquire before trying to tackle more complicated things.

I made few mistakes along the way which prevented the model from reaching the level of accuracy mentioned in the paper.
1. Forgot to add Relu Activation after the first convolutional layer..Duh !
2. I applied the data augmentation transforms such as random horizontal flip and crop  to the test images as well by mistake.
3. I reduced the learning rate during training way too early. 

You can find my implementation [here](https://github.com/kkunte/computer_vision/blob/master/ResNet_CIFAR10.ipynb)

Here are other implementations that I found useful:
<https://github.com/kuangliu/pytorch-cifar/tree/master/models> 
<https://github.com/akamaster/pytorch_resnet_cifar10> 
