---
layout: post
title:  "Panoramic Image Sticher- Computer Vision/OpenCV"
author: "Steven"
---


This is implemented in C++ using Open CV. All the stiching, interest point, feature descriptors are done manually. I only use opencv to put the data in a common format(Mats).

[See On Github](https://github.com/tucci/comp442-compiler)

##  The Challenges
- Extract interest points using a harris detector
- Implement feature descriptors using SIFT
- Implement feature matching using Sum Squared Differences
- Compute homography matrix from matches using RANSAC
- Stich the images together using the homography matrix to a single large panorama image
- Blend the stiched images to get rid of stiching seams across images.


## The Outcome
![](/assets/computer_vision/points_1.png){: .col-12}
Original left image with feature descriptors detected

![](/assets/computer_vision/points_2.png){: .col-12}
Original right image with feature descriptors detected

![](/assets/computer_vision/matches.png){: .col-12}
Simple SSD on the feature descriptors matched

![](/assets/computer_vision/filtered_matches.png){: .col-12}
RANSAC applied to the matches for a higher quality match

![](/assets/computer_vision/stiched.png){: .col-12}
Final Stiched image, with some simple image blending


