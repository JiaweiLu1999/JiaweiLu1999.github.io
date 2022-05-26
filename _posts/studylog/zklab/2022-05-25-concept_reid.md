---
layout:   post
title:    "[ZK Lab] #6: Concept - Re-identification"
subtitle: "BLOG + LINK"
category: studylog
tags: zklab
---

# [ZK Lab] #6: Concept - Re-identification

## Definition
Person re-identification (Re-ID) aims at retrieving a person of interest across multiple non-overlapping cameras.

## Previous Work
### [Re-identification Based on Direct Linear Transform](https://docs.google.com/document/d/1D8OzTOfXJi62jOoa7rm4GZXMlpZbsgyxPaNRN2eSjFA) 

@author: Chenbo Zang

Intro: The project proposed and experimented reidentification between first and second floor cameras by performing 3D coordinate reconstruction using direct linear transform (DLT). Camera calibration, Yolov4 detection and deepsort tracking models are adopted from previous work. The feasibility of the proposed method was validated in small scale experiments, and generalizability was tested on self-constructed dataset with unsatisfactory outcome due to poor calibration, naive distance metrics and susceptible assignment algorithm. New methodologies are required for future work.

### [Unsupervised re-identification in intersections](https://docs.google.com/document/d/16sdFSG-x9RjIrUeexb57Dh0AVXAMqG1_z-sIhj8dvio) 

@author: Mingzhe Hu

Intro: We built an unsupervised re-identification model for first and second camera intersection re-identification of pedestrians and vehicles. We used DukeMTMC and Veri-776 as training sets and constructed a customized test set from synchronized video recordings. We leveraged both CNN and transformer as Reid's backbone and inference tricks to enhance performance. We achieved mAP of 73.3% in vehicle Reid and 89.2% in person Reid, with an inference speed of 25.26 images/sec for vehicle Reid and 31.18 images/sec for person Reid. Code can be accessed on GitHub.

## UCF Related Work

UCF (University of Central Florida) Centerfor Research in Computer Vision has a project named [Multi-Camera Video Analysis](https://www.crcv.ucf.edu/projects/multi-camera.php).

## AiFi Paper

[Cross-View Tracking for Multi-Human 3D Pose Estimation at over 100 FPS](https://openaccess.thecvf.com/content_CVPR_2020/papers/Chen_Cross-View_Tracking_for_Multi-Human_3D_Pose_Estimation_at_Over_100_CVPR_2020_paper.pdf).

### Abstract
Estimating 3D poses of multiple humans in real-time is a classic but still challenging task in computer vision. Its major difficulty lies in the ambiguity in cross-view association of 2D poses and the huge state space when there are multiple people in multiple views. In this paper, we present a novel solution for multi-human 3D pose estimation from multiple calibrated camera views. It takes 2D poses in different camera coordinates as inputs and aims for the accurate 3D poses in the global coordinate. Unlike previous methods that associate 2D poses among all pairs of views from scratch at every frame, we exploit the temporal consistency in videos to match the 2D inputs with 3D poses directly in 3-space. More specifically, we propose to retain the 3D pose for each person and update them iteratively via the cross-view multi-human tracking. This novel formulation improves both accuracy and efficiency, as we demonstrated on widely-used public datasets. To further verify the scalability of our method, we propose a new large-scale multihuman dataset with 12 to 28 camera views. Without bells and whistles, our solution achieves 154 FPS on 12 cameras and 34 FPS on 28 cameras, indicating its ability to handle large-scale real-world applications. The proposed dataset will be released at [https://github.com/longcw/crossview_3d_pose_tracking](https://github.com/longcw/crossview_3d_pose_tracking).


## CPS-IoT Week Competition
 Github [[Link]](https://github.com/JoaoDiogoFalcao/AutoCheckout)
- This repository will help you get started with examples on how to use the Public Datasets available at http://aifi.io/research under Sample Data.
- To start please download the data labelled as: "Simple Example" without depth (For your first example).
- During the competition you will need a competitor token that will distinguish your submission from all other competitors. However you do
not need this token for your local testing environment.

## Attention & Vision Transformer

<iframe width="735" height="450" src="https://www.youtube.com/embed/YAgjfMR9R_M" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

