---
layout:   post
title:    "[ZK Lab] #5: Tool - Prior Projects"
subtitle: "BLOG + LINK"
category: studylog
tags: zklab
---

# [ZK Lab] #5: Tool - Prior Projects

## Outline
- [2022 Spring](#2022-spring)
    - [Re-identification Based on Direct Linear Transform](#re-identification-based-on-direct-linear-transform)
    - [Unsupervised re-identification in intersections](#unsupervised-re-identification-in-intersections)
- [2021 Fall](#2021-fall)  
    - [Face and License Plate Blurring in Street Level Intersection Videos](#face-and-license-plate-blurring-in-street-level-intersection-videos)
    - [Data Augmentation with Causal Inference to Improve Small Object Detection](#data-augmentation-with-causal-inference-to-improve-small-object-detection)
    - [2-Stage (2D and 3D) Approach for Small Pedestrian Detection](#2-stage-2d-and-3d-approach-for-small-pedestrian-detection)
- [2021 Summer](#2021-summer)  
    - [Using Data Augmentation to Improve Pedestrian Detection](#using-data-augmentation-to-improve-pedestrian-detection)
    - [Efficient Det: Comparative Study](#efficient-det-comparative-study)
    - [Software engineering support for RTSP streaming Deepstream pipeline](#software-engineering-support-for-rtsp-streaming-deepstream-pipeline)
    - [COSMOS Vehicle Counting Stage Report](#cosmos-vehicle-counting-stage-report)
- [2021 Spring](#2021-spring)  
    - [Using Data Augmentation to Improve Pedestrian Detection](#using-data-augmentation-to-improve-pedestrian-detection-1)
    - [Face and License Plate Blurring for COSMOS Traffic Intersection](#face-and-license-plate-blurring-for-cosmos-traffic-intersection)
- [2020 Fall](#2020-fall)  
    - [Multi-Resolution and Density Study for Object Detection using YOLOv4](#multi-resolution-and-density-study-for-object-detection-using-yolov4)
    - [Injection of EfficientDet model into Object Detection Pipeline and setting VPN to connect any device to the COSMOS server](#injection-of-efficientdet-model-into-object-detection-pipeline-and-setting-vpn-to-connect-any-device-to-the-cosmos-server)
    - [Research about SSD-832 Adjustment, Non-Maximum Suppression and TensorRT Conversion](#research-about-ssd-832-adjustment-non-maximum-suppression-and-tensorrt-conversion)
    - [Research about bounding box transformation 832 for Multi-camera-fusion , Resolution Study and Density Study](#research-about-bounding-box-transformation-832-for-multi-camera-fusion--resolution-study-and-density-study)
- [2020 Summer](#2020-summer)  
    - [Profiling and Deploying Mask R-CNN with TensorRT and Deepstream](#profiling-and-deploying-mask-r-cnn-with-tensorrt-and-deepstream)
    - [Research about bounding box transformation for multiple cameras fusion, Robust PCA implementation and cropping images for YOLOv4](#research-about-bounding-box-transformation-for-multiple-cameras-fusion-robust-pca-implementation-and-cropping-images-for-yolov4)
    - [Object Detection with Temporal Information](#object-detection-with-temporal-information)
    - [2020 Summer Report: Tracking](#2020-summer-report-tracking)
    - [Data Management using DVC (Data Version Control)](#data-management-using-dvc-data-version-control)
    - [2020 Summer Report: Tracking with FairMOT](#2020-summer-report-tracking-with-fairmot)
    - [DeepStream Deployment and Custom SSD Object Detection Model](#deepstream-deployment-and-custom-ssd-object-detection-model)
    - [Research Report on Data Management Using DVC (Data Version Control)](#research-report-on-data-management-using-dvc-data-version-control)
    - [Single Shot Multibox Detector (SSD) Implementation for Traffic Intersection](#single-shot-multibox-detector-ssd-implementation-for-traffic-intersection)
    - [Summer 2020 Report: Measurements for Object Detection and Tracking for COSMOS Smart Intersections](#summer-2020-report-measurements-for-object-detection-and-tracking-for-cosmos-smart-intersections)
    - [COSMOS Traffic Intersection Research Final report](#cosmos-traffic-intersection-research-final-report)




## 2022 Spring

### [Re-identification Based on Direct Linear Transform](https://docs.google.com/document/d/1D8OzTOfXJi62jOoa7rm4GZXMlpZbsgyxPaNRN2eSjFA) 

@author: Chenbo Zang

#### Abstract
The project proposed and experimented reidentification between first and second floor cameras by performing 3D coordinate reconstruction using direct linear transform (DLT). Camera calibration, Yolov4 detection and deepsort tracking models are adopted from previous work. The feasibility of the proposed method was validated in small scale experiments, and generalizability was tested on self-constructed dataset with unsatisfactory outcome due to poor calibration, naive distance metrics and susceptible assignment algorithm. New methodologies are required for future work.

#### Keywords
re-identification, DLT, Yolov4, deepsort


### [Unsupervised re-identification in intersections](https://docs.google.com/document/d/16sdFSG-x9RjIrUeexb57Dh0AVXAMqG1_z-sIhj8dvio) 

@author: Mingzhe Hu

#### Abstract
We built an unsupervised re-identification model for first and second camera intersection re-identification of pedestrians and vehicles. We used DukeMTMC and Veri-776 as training sets and constructed a customized test set from synchronized video recordings. We leveraged both CNN and transformer as Reid's backbone and inference tricks to enhance performance. We achieved mAP of 73.3% in vehicle Reid and 89.2% in person Reid, with an inference speed of 25.26 images/sec for vehicle Reid and 31.18 images/sec for person Reid. Code can be accessed on GitHub.

#### Keywords
unsupervised learning, re-identification

## 2021 Fall

### [Face and License Plate Blurring in Street Level Intersection Videos](https://drive.google.com/file/d/1rxqgTZA0x-dmiXHPGvFCgDXIK6OPTqMS) 

@author: Alex Angus, Zhuoxu Duan, Adit Deshmukh

#### Abstract
Project COSMOS relies heavily on large image datasets that are gathered from street-level cameras. In the process of collecting real-time images and videos of public spaces, cameras also inadvertently capture sensitive information such as faces and license plates. To avoid the compromise of large amounts of private information in the followup research involving our image datasets, we generate a pipeline to systematically blur the faces of pedestrians and the license plates of vehicles in street level intersection videos. We train various YOLOv4 object detection models, using the Darknet framework, for the detection of pedestrians and vehicles as well as for the detection of faces and license plates. We train the models with our own custom intersection video dataset annotated Summer 2021. Additionally, we implement two models, MobileNetV3 and WPOD-net, for the detection of faces and license plates, respectively. The face detection model performs well with a mean IoU above 70% on our COSMOS dataset while the license plate model still has some problems since the confidence loss in training tends to be stuck at 36.048. Ultimately, we are able to automatically blur 99% of visible faces and license plates in any given 1st floor intersection video.

#### Keywords
face blurring, license plate blurring, object detection

### [Data Augmentation with Causal Inference to Improve Small Object Detection](https://docs.google.com/document/d/1WtgWKL8gWHjtdCmXvNerKf9fNt9bwhXlrnjiu8yLqZQ)

@author: Lingxiao Li

#### Abstract
Causal inference is a critical research topic across many domains for decades. Nowadays, estimating causal effects from observational data has become an appealing research direction owing to the large amount of available data and low budget requirement, compared with randomized controlled trials. At the same time, small object detection remains a challenging task in deep learning. In this project, we aim to study the causal effect from observational data to the performance of the YOLOv4 model on small object(pedestrian) detection and use data augmentation to improve the accuracy of pedestrian detection using causal inference methods. Our evaluation results show that the average precision for pedestrians of the model trained by the augmented data and unaugmented data improves 67.89%  compared to the average precision of the model only trained by the unaugmented data, which indicates that our approach successfully improved the accuracy of small object detection of the YOLOv4 model by decorrelate co-founders in training dataset.

#### Keywords
causal inference, data augmentation, small object detection


### [2-Stage (2D and 3D) Approach for Small Pedestrian Detection](https://docs.google.com/document/d/1Tp3CQ2Dl8hqGf-9WBlW5wnt5Cg55aAKxnZlVxWqSnl8)

@author: Sung Jun Won

#### Abstract
Small object detection remains a challenging task in deep learning. In this project, we primarily attempted to replicate the work done in Dogfight: Detecting Drones from Drones Videos. We experimented with both the spatial model and the spatio-temporal model using the 12th floor videos dataset. For the spatial model, we divided each frame into 9 overlapping regions to account for the small size of pedestrians compared to the whole image. PSPNet is then trained on the cropped images and the ground truth images. For the spatio-temporal model, in order to discover pedestrian locations, we generated motion boundaries images and tracked candidate pedestrian locations for a few frames using cuboids. Then, the Inflated 3D model is used to extract the 3D convolution feature maps for the model to train on. We ended up not producing meaningful results for the experiments due to many technical challenges regarding the model overfitting and interpreting the model architecture. 

#### Keywords
PSPNet, Overlapping regions, Conditional Random Fields, Convolution features, Inflated 3D

## 2021 Summer

### [Using Data Augmentation to Improve Pedestrian Detection](https://docs.google.com/document/d/1MN5BJrRNADjJCHNc5TMKTbK1df6bJx6-y60whkBzmAw)

@author: Sung Jun Won, Shambhavi Roy

#### Abstract
You Only Look Once (YOLO) is deemed a state-of-the-art model for object detection today. In this project, images taken from the 12th floor of the Mudd building are used, and detecting pedestrians is the primary challenge. A scarce number of pedestrians in each frame causes class imbalance as the vehicles outnumber pedestrians in many frames. Also, pedestrians are very small in size compared to the size of each frame. To resolve these problems and perform pedestrian detection successfully, we have experimented with data augmentation and finally achieved realistic data augmentation by rescaling. The main goal of our project is to evaluate this augmentation technique in 832 x 832 images using the YOLOv4 model for any improvement in performance. The current results indicate that there’s an error in training, demonstrated by the unrealistically high AP results - 100% for vehicles and nearly 100% for pedestrians when trained with an unaugmented dataset .

#### Keywords
Data augmentation, Small object detection, Pedestrian detection, Darknet, YOLOv4

### [Efficient Det: Comparative Study](https://docs.google.com/document/d/13x432QAHevbpWDZiR8qLdnDVngrmJ_-b)

@author: Adit Deshmukh, Tushar Gupta

#### Abstract
EfficientDet is a novel deep-learning framework that aims at developing a formal approach towards scaling object detection networks in terms of parameters and speed. Our work explores the network’s performance on the 12th floor and Visdrone 2019 dataset. We aim to develop an accurate and efficient object detection pipeline using the work done on EfficientNet as the backbone. We obtained the highest MAP of 0.7 with the 12th-floor dataset.

#### Keywords
scaling coefficient, object-detection, Bi-directional Feature pyramid network, Efficient Net


### [Software engineering support for RTSP streaming Deepstream pipeline](https://docs.google.com/document/d/1W7MQMVM0I9u47I-ctbmNgT-Fr-fucKas)

@author: Tushar Gupta

#### Abstract
The project involved working on various components of an RTSP streaming pipeline that enables distributed interference in support of video-based object detection and tracking. Tasks included software engineering in support of networked streaming to enable frame synchronization, latency measurements, and video segmentation. 

#### Keywords
Deepstream, GStreamer, Video streaming, FFmpeg


### [COSMOS Vehicle Counting Stage Report](https://docs.google.com/document/d/1OWbmhPi6h6ceY16eAK_PBIcGwjFxQlR0o-mqueWdQpU)

@author: Lingxiao Li, Xingxing Geng

#### Abstract
One of the important goals for the COSMOS (Cloud Enhanced Open Software-Defined Mobile Wireless Testbed) project is analyzing traffic flow in real time. To achieve this goal, we need to count and classify vehicles and pedestrians crossing the traffic intersection. This report summarizes the work we have done for the 2021 summer. We applied YOLOv4 which was implemented in PyTorch with pre-trained Darknet YOLOv4 models to detect objects in 832x832 cropped videos. We utilize the DeepSORT algorithm to track objects. We designed a simple but efficient algorithm to classify vehicles by their directions and turning movements. We evaluated the performance of our model on 12th floor videos using MOT metrics. We designed a piece of software which can be used on 12th floor cameras. The average accuracy for 12 test videos is 95% which satisfies the requirement for this project.  The limiting factors are the small object detection. 

#### Keywords
Object Detection, Object Tracking, Object Counting, Yolov4


## 2021 Spring 

### [Using Data Augmentation to Improve Pedestrian Detection](https://docs.google.com/document/d/1mNmre_IdVJ7WUGaeYMASNb8_d3qMfCazQR09iGyvB4c)

@author: Kevin Murning

#### Abstract
Robust detection of small objects in large videos and images remains a significant challenge in the field of object detection. In the case of the Cosmos traffic intersection research, this challenge is present in the task of robust detection of pedestrians. The reasons for this are two-fold. First, the pedestrians present in the 1080p images only occupy a very small pixel range. Second, there is a significant class imbalance present in the data. The number of pedestrians present is far less than the number of vehicles. The objective of this study is to evaluate the efficacy of  a data augmentation technique in improving the detection of pedestrians. Software was written to artificially augment the number of pedestrians present in the data. This dataset was then used to train YOLOv4. It was found that using a combination of augmented and unaugmentated data in training YoloV4 improved the average precision of detecting pedestrians by 8.61% in comparison to a model trained only on the unaugmented data. 

#### Keywords
Small Object Detection, Data Augmentation, YOLOv4


### [Face and License Plate Blurring for COSMOS Traffic Intersection](https://docs.google.com/document/d/1UvYZEFo7y8Dh5z2uuK8r7NtkgyXUUNJ-sTXi5a8fP5w)

@author:  Zhuoxu Duan, Jingyuan Liu, Wenjun Chen, Joseph Yang, Zoran Kostic

#### Abstract
Project COSMOS relies heavily on the large image datasets that are gathered from street-level cameras. In the process of collecting the real-time images/videos of public spaces, the cameras also inevitably captured information like licence plates, faces, and many other information that would be considered sensitive from a privacy perspective. To avoid compromise of massive personal information in the follow-up research that works with our image dataset, we need to blur the images on pedestrian faces and license plates. In this project, we present a system that combines object detectors like Yolov4 and Mask RCNN with manually trained CNN to blur the sensitive areas of an image/video. We also carefully designed a series of annotation rules on first-floor camera videos and created an annotated first-floor camera image dataset with the annotation rules.

#### Keywords
face blurring, license plate blurring, image annotation, object detection

## 2020 Fall

### [Multi-Resolution and Density Study for Object Detection using YOLOv4](https://docs.google.com/document/d/1wAtXJjL9FVSu-Itc1hiAFp_82SgNzFN88jX8w5Kbtts)

@author: Richard Samoilenko, Dwiref Oza, Ashvin Jagadeesan

#### Abstract
Deploying deep learning inference for object detection with video streaming presents significant challenges involving efficiency. For the task of traffic intersection monitoring, a high throughput, low latency pipeline is essential for accurate real time detection. Our tasks were to determine object detection performance with YOLOv4 trends with different video resolutions, square vs. 16:9 aspect ratios; and finally object densities on a per-frame basis. Our results indicate clear trends in how each input resolution and aspect ratio affect inference. All results are supported with CUDA profiling, through which we also found that the lab’s Hikvision cameras give better results than GoPro videos. We also report some linear trends in how object density may affect inference times.

#### Keywords
traffic intersection, object detection, YOLOv4, CUDA, profiling, resolution, object density


### [Injection of EfficientDet model into Object Detection Pipeline and setting VPN to connect any device to the COSMOS server](https://docs.google.com/document/d/1vIgWTE-n0fGd6TABP6hEJL7-0V0z18Zo5oRCpL4E4wI)

@author: Vedant Dave

#### Abstract
This report aims to highlight the work that has been done throughout the Fall semester. The work has mainly been divided into two parts: 
- Coming up with a way to connect linux based edge devices to the COSMOS server in order to send and receive data.
- Injecting EfficientDet object detection model into the object detection pipeline in order to analyze the performance of the model on the custom traffic intersection dataset.


### [Research about SSD-832 Adjustment, Non-Maximum Suppression and TensorRT Conversion](https://docs.google.com/document/d/1rmjpAsZ_oj6XKx02YJ74l-uvtG8KKt7Isz0ULwM3Mzk)

@author: Zhuoxu Duan, Zoran Kostic

#### Abstract
As part of the smart city, the traffic intersection program is aiming at detecting pedestrians and vehicles on the street to provide further information about crowd density and traffic busyness. The SSD model is chosen to perform this object detection task as well as building up a pipeline with TensorRT and DeepStream for higher inference speed. In this report, we managed to adjust the SSD model to fit our application and conducted model conversions to take advantage of TensorRT. Corresponding profiling results and problems remaining are also discussed.

#### Keywords
Object Detection, Single Shot Multibox Detector (SSD), TensorRT, DeepStream, Smart City



### [Research about bounding box transformation 832 for Multi-camera-fusion , Resolution Study and Density Study](https://docs.google.com/document/d/1jSOkrcT1Ku8p_QkphiHisBF-4KxgRb9aOBS7iVK6Gnc)

@author: Zihao Xiong, Hongzhe Ye
#### Abstract
Smart-city intersections will play an important role in automated traffic management, help protect pedestrians, and decrease the possibility of accidents. Multiple cameras might be useful to either get more information of the position we are looking for or help to improve the accuracy of detection. In this report, the work in the COSMOS project that we have finished in 2020 Fall will be shown. Bounding box transformation for 832 is evaluated. Also, study about performance of YoloV4 in different model settings, input size and density is presented. 

## 2020 Summer

### [Profiling and Deploying Mask R-CNN with TensorRT and Deepstream](https://docs.google.com/document/d/1bF9VKhOJuCHwq7WlV2c_QNsT1RHJWf73MY5ASDPIU3I)
@author: Ananye Pandey 
#### Abstract
Deploying deep learning inference for object detec tion with video streaming presents significant challenges involving efficiency. For the task of traffic intersection monitoring, a high throughput, low latency pipeline is essential for accurate real time detection. Our task was to learn and demonstrate how to convert a trained Mask R-CNN model into a serialized TensorRT .engine, profile inference on a CUDA dGPU, optimize the engine where needed, and then deploy the engine within the Nvidia Deepstream SDK pipeline, a streaming analytics toolkit. In this report, we outline the key elements of our work, namely the Mask R-CNN network, CUDA profiling, setting up the right working environment, some pitfalls to be avoided with regards to package versioning, TensorRT and UFF engine conversion, and deploying the model with Deepstream. This work was done during the Summer of 2020, for the Traffic Intersection research project under COSMOS. 
#### Keywords
Mask R-CNN, CUDA, TensorRT, nvprof, profil ing, Deepstream, Tensorflow, docker 


### [Research about bounding box transformation for multiple cameras fusion, Robust PCA implementation and cropping images for YOLOv4](https://docs.google.com/document/d/1bF9VKhOJuCHwq7WlV2c_QNsT1RHJWf73MY5ASDPIU3I)
@author: Hongzhe Ye
#### Abstract
Smart-city intersections will play an important role in automated traffic management, help protect pedestrians, and decrease the possibility of accidents. Multiple cameras might be useful to either get more information of the position we are looking for or help to improve the accuracy of detection. In this report, the work in the COSMOS project that I have finished in 2020 Summer will be shown. Based on new calibration, Bounding box transformation can help combine information from two cameras. Also, experiment of Robust PCA background subtraction and cropping images for YOLOv4 is represented.

### [Object Detection with Temporal Information](https://docs.google.com/document/d/1oTVBDE3s-sbcprsyv8LcSHr50SoQRH0_o7g4zFR3vIU)
@author: Jeswanth Yadagani
#### Abstract
This report includes information about various Temporal Yolo models that we have tried during summer 2020. Improving the detection accuracy of pedestrians is our main objective. By leveraging temporal information, there is a high chance of improvement in terms of object detection when we have a static background. Certain models in this fashion are explored in this report and the directions in which this study can be taken forward are explained at the end. Also, a structured environment has been created for coming up with new architectures and evaluating performance of each model.

### [2020 Summer Report: Tracking](https://docs.google.com/document/d/1e0wGHWpvy1OgaXrqtF8SeLaEU42ak_OjpgB8rr1E7l0)
@author: Mingfei Sun
#### Abstract
In this report, I will discuss work accomplished during the 2020 Summer on the Traffic Intersection research project, under COSMOS. Mainly three things, discriminative correlation filter-based (DCF) tracker, FairMOT tracker, and some other useful experiments.
#### Keywords
Tracking, DCF tracker, FairMOT, DeepStream

### [Data Management using DVC (Data Version Control)](https://docs.google.com/document/d/1-lh9PRnH3KRC6nYyMNROdoCXP21I4kU2)
@author: Tian Yang
#### Abstract
In this report, we will discuss the data management work of machine learning models using DVC (Data Version Control). We first introduce the background, explain why this tool is needed and helpful to be applied on ML projects, then introduce the basic working principles of DVC and part of the workflow of the neural network, YOLO darknet, that will be involved in our experiment. Next we detail the steps of generating stages, connecting them as pipeline, tagging experiments and comparisons of metrics. We end this report by outlining recommended next steps for future work.
#### Keywords
Data Management, Data Versioning Tool, DVC

### [2020 Summer Report: Tracking with FairMOT](https://docs.google.com/document/d/1fkSgKhrnxFJmCinJpXydUrUMzUTrGUIzVbCfOwkBFKY)
@author: Yi Chen
#### Abstract
This report summarizes the accomplishments in 2020 Summer for tracking in the COSMOS Traffic Intersection research project. FairMOT is  a new open source tracking algorithm proposed by the paper ’A Simple Baseline for Multi-Object Tracking’ in 2020. The main tasks of my work is to implement FairMOT to achieve better vehicles and pedestrians tracking performance in our Traffic Intersection project. 

### [DeepStream Deployment and Custom SSD Object Detection Model](https://docs.google.com/document/d/11FtuNB_kXLcVfLeItCQs7VaAUUOCAMvFoK-u5oJUU4g)
@author: Yiping Pan
#### Abstract
Traffic Intersection project’s goal is to implement fast object detection and tracking of vehicles and pedestrians on videos collected from real  traffic intersections. In the object detection part, one of the most popular algorithms SSD hasn’t been implemented by our lab researchers. We at the first time built the SSD model on our own so that it provides a good base for researchers to do further improvement, training and testing for SSD-based algorithms. Our trained fine-tuned VGG-SSD model is able to detect the object with an acceptable average precision and it is promising to obtain better results when investing more research on that. On the other hand, we also provide analysis and test on Nvidia DeepStream SDK where we could implement custom YoloV3 and build accelerated video processing pipelines. A well-organized summary of DeepStream configuration concepts and methods is also created.
#### Keywords
SSD, YoloV3, DeepStream5.0, Object Detection

### [Research Report on Data Management Using DVC (Data Version Control)](https://docs.google.com/document/d/1DU236v_eak9dC1K8wVv4Vl4axlK3zgAJ24q4p2nAu_E)
@author: Yanqi Zheng
#### Abstract
DVC can bring agility, reproducibility, and collaboration into the existing data flow. To ease data management, we implement DVC features like storage agnostic, reproducible, and metric tracking. 

According to our study, there are mainly two problems we can fix if implementing DVC in the current YOLO model. One is data versioning, solved by using DVC to keep track of different versions of data. Another is data lineage, solved by constructing deep learning pipelines with DVC. 

DVC improves collaboration among deep learning developers. It helps them to keep a well-organized collection of data sets and allows them to share data versions with each other. It also provides an efficient way to reproduce experiments and show a comparison between different models.

### [Single Shot Multibox Detector (SSD) Implementation for Traffic Intersection](https://docs.google.com/document/d/1tDipRQKaZ9v3pLIQcHNasX_9AjwFW_k6tcMUSkrS02A)
@author: Zhuoxu Duan
#### Abstract
This report first makes a description of the current stage of the traffic intersection program. Expectations for the SSD group are clarified. For the DeepStream model conversion task, the report introduced the motivation, possible procedures and challenges of various ways to move SSD models to DeepStream. Finally succeeded in converting PyTorch models to DeepStream plugins. For the custom & training task, SSD model structure, data flow details and prediction principles are illustrated. Implemented SSD300 models with both VGG16 and ResNet50 backbones on PyTorch. Data preparation and feature mining was done for our traffic dataset with the following training processes. Large parts of vehicles can be detected while few pedestrians are recognized. Example results and reasoning for the failure are presented.
#### Keywords
object detection, Single Shot Multibox Detector (SSD), DeepStream


### [Summer 2020 Report: Measurements for Object Detection and Tracking for COSMOS Smart Intersections](https://docs.google.com/document/d/1kQxKhYx2DeSAZT6LpTT87QXxGOltnPinwvH_44qE9KA)
@author: Zihao Xiong
#### Abstract
In this report, we will discuss work accomplished from May - August 2020 on the lab’s custom measurement code supporting both object detection and tracking models. We first detail the performance improvements made for both detection measurement and multiple object tracking measurement, each of which now runs approximately 80-90% faster. We next describe the diagnosis and fix of a critical error found in the original detection measurement code. This work also yielded full coverage unit testing for the detection measurement code and additional visualization tooling in support of understanding detection measurement metrics. However, there remain important open questions and therefore there is still work to be done. We end this report by outlining recommended next steps for work on the lab’s native measurement code.

### [COSMOS Traffic Intersection Research Final report](https://docs.google.com/document/d/1GYK7ALfPJ3hdZoWXaljmG52uqOjUwkGP3SP7jm-ulbg)
@author: Zhengye Yang
#### Abstract
This report summarizes the work done during 2020 summer term. In this report, the following fields will be described: 
- (i) The summary of COSMOS traffic intersection current process. 
- (ii) Social distancing analysis system (SDAS). 
- (iii) Current status towards real-time detection. 

This report can be seen as a summary of the current status of COSMOS smart intersection research. 
#### Keywords
COSMOS traffic intersection, object detection, social distancing ,  real-time implementation.







## Reference
[1] [Re-identification Based on Direct Linear Transform](https://docs.google.com/document/d/1D8OzTOfXJi62jOoa7rm4GZXMlpZbsgyxPaNRN2eSjFA)

[2] [Unsupervised re-identification in intersections](https://docs.google.com/document/d/16sdFSG-x9RjIrUeexb57Dh0AVXAMqG1_z-sIhj8dvio)

[3] [Face and License Plate Blurring in Street Level Intersection Videos](https://drive.google.com/file/d/1rxqgTZA0x-dmiXHPGvFCgDXIK6OPTqMS) 

[4] [Data Augmentation with Causal Inference to Improve Small Object Detection](https://docs.google.com/document/d/1WtgWKL8gWHjtdCmXvNerKf9fNt9bwhXlrnjiu8yLqZQ)

[5] [2-Stage (2D and 3D) Approach for Small Pedestrian Detection](https://docs.google.com/document/d/1Tp3CQ2Dl8hqGf-9WBlW5wnt5Cg55aAKxnZlVxWqSnl8)

[6] [Using Data Augmentation to Improve Pedestrian Detection](https://docs.google.com/document/d/1MN5BJrRNADjJCHNc5TMKTbK1df6bJx6-y60whkBzmAw)

[7] [Efficient Det: Comparative Study](https://docs.google.com/document/d/13x432QAHevbpWDZiR8qLdnDVngrmJ_-b)

[8] [Software engineering support for RTSP streaming Deepstream pipeline](https://docs.google.com/document/d/1W7MQMVM0I9u47I-ctbmNgT-Fr-fucKas)

[9] [COSMOS Vehicle Counting Stage Report](https://docs.google.com/document/d/1OWbmhPi6h6ceY16eAK_PBIcGwjFxQlR0o-mqueWdQpU)

[10] [Using Data Augmentation to Improve Pedestrian Detection](https://docs.google.com/document/d/1mNmre_IdVJ7WUGaeYMASNb8_d3qMfCazQR09iGyvB4c)

[11] [Face and License Plate Blurring for COSMOS Traffic Intersection](https://docs.google.com/document/d/1UvYZEFo7y8Dh5z2uuK8r7NtkgyXUUNJ-sTXi5a8fP5w)

[12] [Multi-Resolution and Density Study for Object Detection using YOLOv4](https://docs.google.com/document/d/1wAtXJjL9FVSu-Itc1hiAFp_82SgNzFN88jX8w5Kbtts)

[13] [Injection of EfficientDet model into Object Detection Pipeline and setting VPN to connect any device to the COSMOS server](https://docs.google.com/document/d/1vIgWTE-n0fGd6TABP6hEJL7-0V0z18Zo5oRCpL4E4wI)

[14] [Research about SSD-832 Adjustment, Non-Maximum Suppression and TensorRT Conversion](https://docs.google.com/document/d/1rmjpAsZ_oj6XKx02YJ74l-uvtG8KKt7Isz0ULwM3Mzk)

[15] [Research about bounding box transformation 832 for Multi-camera-fusion , Resolution Study and Density Study](https://docs.google.com/document/d/1jSOkrcT1Ku8p_QkphiHisBF-4KxgRb9aOBS7iVK6Gnc)

[16] [Profiling and Deploying Mask R-CNN with TensorRT and Deepstream](https://docs.google.com/document/d/1bF9VKhOJuCHwq7WlV2c_QNsT1RHJWf73MY5ASDPIU3I)

[17] [Research about bounding box transformation for multiple cameras fusion, Robust PCA implementation and cropping images for YOLOv4](https://docs.google.com/document/d/1bF9VKhOJuCHwq7WlV2c_QNsT1RHJWf73MY5ASDPIU3I)

[18] [Object Detection with Temporal Information](https://docs.google.com/document/d/1oTVBDE3s-sbcprsyv8LcSHr50SoQRH0_o7g4zFR3vIU)

[19] [2020 Summer Report: Tracking](https://docs.google.com/document/d/1e0wGHWpvy1OgaXrqtF8SeLaEU42ak_OjpgB8rr1E7l0)

[20] [Data Management using DVC (Data Version Control)](https://docs.google.com/document/d/1-lh9PRnH3KRC6nYyMNROdoCXP21I4kU2)

[21] [2020 Summer Report: Tracking with FairMOT](https://docs.google.com/document/d/1fkSgKhrnxFJmCinJpXydUrUMzUTrGUIzVbCfOwkBFKY)

[22] [DeepStream Deployment and Custom SSD Object Detection Model](https://docs.google.com/document/d/11FtuNB_kXLcVfLeItCQs7VaAUUOCAMvFoK-u5oJUU4g)

[23] [Research Report on Data Management Using DVC (Data Version Control)](https://docs.google.com/document/d/1DU236v_eak9dC1K8wVv4Vl4axlK3zgAJ24q4p2nAu_E)

[24] [Single Shot Multibox Detector (SSD) Implementation for Traffic Intersection](https://docs.google.com/document/d/1tDipRQKaZ9v3pLIQcHNasX_9AjwFW_k6tcMUSkrS02A)

[25] [Summer 2020 Report: Measurements for Object Detection and Tracking for COSMOS Smart Intersections](https://docs.google.com/document/d/1kQxKhYx2DeSAZT6LpTT87QXxGOltnPinwvH_44qE9KA)

[26] [COSMOS Traffic Intersection Research Final report](https://docs.google.com/document/d/1GYK7ALfPJ3hdZoWXaljmG52uqOjUwkGP3SP7jm-ulbg)