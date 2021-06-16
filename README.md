# Floating Plastic Debris Detection with Deep Learning and Computer Vision
This repository includes all the code and notebooks that I used for the content of my MSc thesis. The content revolves around the detection of floating plastic debris in waterways with computer vision and deep learning techniques. Therefore experiments were carried out with static cameras and mobile phones to capture videos of floating plastic debris. 

Please send a mail to andrevallendar95@gmail.com, if you want to have access to all the data (image classification and object detection).

## Table of contents
* [Pre-processing](#Pre-processing)
* [Image Classification](#Image-Classification)
* [Object Detection YOLOv4](#Object-Detection)
* [Model weights for Image Classification and Object Detection](#Model-weights-for-Image-Classification-and-Object-Detection)
	
## Pre-processing
The audio of a GoPro video can be extracted by the following (Anaconda prompt)

```
$ ffmpeg -i **VIDEOFILE PATH**.MP4 -vcodec copy -an **NEW VIDEOFILE PATH**.MP4
```
Afterwards the VideoToImage tool can be used to extract images from a video. This tool can be found in the folder 'image classification' --> 'pre-processing'

## Image Classification
The model accuracies for the detection of plastic debris for a from scratch built baseline model and five state-of-the-art algorithms was done in the Tensorflow and Keras libraries. The notebooks can be found in in the 'image classification' folder. For carrying out the computations the notebook should be uploaded to Google Drive to run the notebook via Google Colab (enable the GPU). 
For training with **pre-trained weights** and **from scratch** in the 'Transfer Learning for four classes' notebook, set **model.trainable=False** or **model.trainable=True** respectively. 
The model results are are presnted below (training and testing on 2.7m/0 deg):


| Model      | Pre-trained weights | Training from scratch |
| ---------- | ------------------- | -------------------   |
| Baseline   | 		-          |		78.9%      |
| ResNet50   | 		45.4%      |		82.4%	   |
| InceptionV3| 		54.6%      |		81.5%	   |
| DenseNet121| 		62.7%      |		87.6%      |
| MobileNetV2| 		60.7%      |		75.0%      |
| SqueezeNet | 		66.7%      |		73.9%      |

## Object Detection

To run the YOLOv4 model as object detector, the notebook and guidelines from the two following repositories were used:

* https://github.com/theAIGuysCode/YOLOv4-Cloud-Tutorial (Notebook)
* https://github.com/AlexeyAB/darknet (Guidelines)

The adapted notebook with guidelines, steps to follow and needed files can be found in the folder 'object detection'. 

![image](https://user-images.githubusercontent.com/85031780/120117964-4a3e9980-c190-11eb-906b-0631b72fd441.png)

## Model weights for Image Classification and Object Detection

The model weights for image classification and object detection can be downloaded via the following link:

The model weights for image classification can be used to replicate the confusion matrices and to get the statistics. For object detection the weights can be used to get predictions for unseen or test images, continue the training process or to get the s and to get the statistics

