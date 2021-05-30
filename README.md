# Floating Plastic Debris Detection with Deep Learning and Computer Vision
This repository comprises all the code and notebooks that I used for the content of my MSc thesis. The content revolves around the detection of floating plastic debris in waterways with computer vision and deep learning techniques.

Please send a mail to andrevallendar95@gmail.com, if you want to have access to all the data and model weights (image classification and object detection)

## Table of contents
* [Pre-processing](#Pre-processing)
* [Image Classification](#Image-Classification)
* [Object Detection YOLOv4](#Object-Detection)
	
## Pre-processing
The audio of a GoPro video can be extracted by the following (Anaconda prompt)

```
$ ffmpeg -i **VIDEOFILE PATH**.MP4 -vcodec copy -an **NEW VIDEOFILE PATH**.MP4
```
Afterwards the VideoToImage tool can be used to extract images from a video. 

## Image Classification
The model accuracies for the detection of plastic debris for a from scratch built baseline model and five state-of-the-art algorithms was done in the Tensorflow and Keras libraries. The notebooks can be found in in the 'image classification' folder. For carrying out the computations the notebook should be uploaded to Google Drive to run the notebook via Google Colab (enable the GPU). 
For training with **pre-trained weights** and **from scratch** in the 'Transfer Learning for four classes' notebook, set **model.trainable=False** or **model.trainable=True** respectively. 
The model results are are presnted below (training and testing on 2.7m and 0 deg):


| Model      | Pre-trained weights | Training from scratch |
| ---------- | ------------------- | -------------------   |
| Baseline   | 		-          |		78.9%      |
| ResNet50   | 		45.4%      |		82.4%	   |
| InceptionV3| 		54.6%      |		81.5%	   |
| DenseNet121| 		62.7%      |		87.6%      |
| MobileNetV2| 		60.7%      |		75.0%      |
| SqueezeNet | 		66.7%      |		73.9%      |
