<!-- ---
layout: post
title: ImageFocus AI Depth-Driven Graded Blurring
date: 2023-11-11 09:56:00-0400
description: 
tags: project
categories: Deep_learning
giscus_comments: false
related_posts: false
featured: false
---


Graded blurring of an image based on how far a point is from focus, achieved solely with a single image and no extra data. Our approach involves generating a depth map for the image using machine learning. Create blurred versions of the image in levels based on how far a point is from the depth of focus, and seamlessly stitch the different blurred images to create the final masterpiece where the selected point remains fully focused while points further away become progressively blurred.

## Depth Estimation
I utilized a method based on the paper "Unsupervised Monocular Depth Estimation with Left-Right Consistency." Discover more about their groundbreaking paper [here](http://visual.cs.ucl.ac.uk/pubs/monoDepth/).
The machine learning model is trained on a large set of stereo (left-right) images to generate a right image from a given left image. By learning internally about the depth of various points in the image, the model is then capable of generating a depth map for a simple image.
 -->
