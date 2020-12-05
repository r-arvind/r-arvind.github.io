---
layout: post
title:  "Tracking Without Bells and Whistles"
author: arvind
categories: [Computer Vision]
tags: [object detector,faster rcnn,object tracking]
image: assets/images/object-tracker.jpg
bannerimage: assets/images/object-tracker.jpg
description: "A new paradigm of object tracker without bells and whistles that is capable of tracking objects using just an object detector"
featured: false
hidden: false
---

This article talks about a completely new paradigm of object tracker. And what's special about this tracker is that it requires only an object detector and nothing else! No additional training or additional algorithm is required for tracking objects. Hence the name tracking without bells and whistles.

You can checkout the complete research paper at [arXiv.org](https://arxiv.org/abs/1903.05625). This article gives an overview of the paper.



## Tracking by detection

Tracking by detection is a paradigm of object tracking algorithm that use an object detector as a basis for performing object tracking. Modern Object detectors such as YOLO and FRCNN are able to achieve extremely high accuracy with very low computation time. Therefore, we might as well use object detectors for performing tracking.

Tracking by detection can be essentially simplified to the following three steps:

1. Perform object detection on frame at time *t*. 

2. Perform object detection on frame at time *t+1*

3. Map the objects detected in frame *t* to the objects detected in frame *t+1*

![Tracking by detection]({{ site.baseurl }}/assets/images/det-tracking.png)

The third step is known as **data association** as it involves associating objects detected in one frame to that of another. There are various algorithms for performing data association. We can also use different types of object detectors for performing the object detection step.  

Several object trackers such as SORT and deepSORT use this paradigm of object tracking. 


## Revisiting Object Detector

In order to understand how this new object tracker works, we need to go back to the basics and understand how single and multiple object detectors work.


### Single Object Detector

In a CNN based object detector, we generally have a VGG backbone network which converts an image into feature maps. We stretch out these features maps into a fully connected layer. 

<!-- ![Object detection with CNN]({{ site.baseurl }}/assets/images/obj-det-cnn.png){ width=50% } -->

<img src="{{ site.baseurl }}/assets/images/obj-det-cnn.png" alt="Object Detection with CNN" />

Then we can use the Fully Connected Layer to perform a classification based on class label and a regression for bounding boxes. You can read more about this on the internet.

When you pass an image to object detector the output looks something like this:

<img src="{{ site.baseurl }}/assets/images/obj-det-res.png" alt="Result of Object Detection with CNN" />

You get a list of bounding boxe coordinates and a class probability attached to it. We pick the one with the highest probability as the output. 


## Multiple Object Detector

Now that we have seen how a single object detector works, let's fast forward to multiple object detection. In this case, we will be looking at Faster RCNN.

An FRCNN is in some ways similar to a single object detector. The only addition is the presence of a Region Proposal Network, which proposes the regions where the likelihood of finding an object is extremely high. Once we get these regions from the RPN, we perform a pooling of the region of interests, and then as usual convert it into a fully connected layer and perform a classification for class label and regression for the bounding boxes.



<img src="{{ site.baseurl }}/assets/images/frcnn.png" alt="Faster RCNN" />
