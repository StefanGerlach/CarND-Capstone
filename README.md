# Capstone Project
Self-Driving Car Engineer Nanodegree Program

[//]: # (Image References)
[image1]: ./imgs/training_trafficlight_sg/training_monitoring.png "moni1"
[image2]: ./imgs/training_trafficlight_sg/training_monitoring2.png "moni2"

[image3]: ./imgs/training_trafficlight_sg/detection1.jpg "detect1"
[image4]: ./imgs/training_trafficlight_sg/detection1b.jpg "detect2"
[image5]: ./imgs/training_trafficlight_sg/detection1c.jpg "detect3"
[image6]: ./imgs/training_trafficlight_sg/detection2.jpg "detect4"
[image7]: ./imgs/training_trafficlight_sg/detection2b.jpg "detect5"
[image8]: ./imgs/training_trafficlight_sg/detection3.jpg "detect6"

[image9]: ./imgs/training_trafficlight_sg/daySequence1.jpg "orig_modality1"
[image10]: ./imgs/training_trafficlight_sg/daySequence1b.jpg "orig_modality2"

[image11]: https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/img/kites_detections_output.jpg "tensorflow_object"


## Training a Traffic Lights Detection and Classification Network

This task is about the perception module of the capstone project of the Udacity Self-Driving Car Engineer Nanodegree Program.

To build up a robust and computational efficient system for traffic light detection and classification based on a deep neural network architecture, one might think about the following points:

- What framework to use for training and inference (TensorFlow can be used in the car environment)
- What neural network architecture to use
- What datasets for training can be used
- How to augment images for creating a robust network
- How to deploy the trained model to the car environment


### Framework

The [Tensorflow Object Detection API](https://github.com/tensorflow/models/tree/master/research/object_detection) is a way to tackle the problem. Next to other really handy frameworks like [Darknet YOLO](https://pjreddie.com/darknet/yolo/), it is easy to use for fast prototyping, training, training monitoring and graph exports.

![detectionAPI][image11]

### Neural Network Architectures

There are several architectures for object detection that have pros and cons. To name some of them:

- Faster RCNN Architectures with different backends (slow but very accurate)
- SingleShotDetectors (SSD) with different backends (very fast but not as accurate)
- You Only Look Once (YOLO) with Darknet backends (fast and accurate)


### Pre-Trained Network

It is usefull to start with a pre-trained network and fine tune it on the specific task. Most networks are pre-trained on object-detection datasets like [COCO Dataset](http://cocodataset.org/#home) 


### Dataset

For this project, I want to use the following datasets for fine tuning:
- [Lisa Traffic Light Dataset](https://www.kaggle.com/mbornoe/lisa-traffic-light-dataset/home)
- [CamVid](http://mi.eng.cam.ac.uk/research/projects/VideoRec/CamVid/)
- [Bosch Small Traffic Lights Dataset](https://hci.iwr.uni-heidelberg.de/node/6132)


### Training


