# Object Detection using YOLOv5 on Custom Dataset.

# Introduction

#### This repository contains code for training and using YOLOv5, a state-of-the-art object detection model, on a custom dataset. YOLOv5 is a real-time object detection model that can detect multiple objects in an image or video.

# Prerequisites

 * Python 3.7 or later
 * PyTorch 1.7 or later
 * CUDA and cuDNN (if using a GPU for training)
 * OpenCV
 * Matplotlib
 * Numpy
 
# Installation
 ### Clone the repository:
 
 ```  git clone https://github.com/<username>/object-detection-using-yolov5-on-custom-dataset.git ```
 
 ### Install the required packages:
 
 ``` pip install -r requirements.txt ```
 
 ### Download the YOLOv5 weights from the official [website](https://github.com/ultralytics/yolov5) and place them in the weights directory.
 


-----------------------------------------------------------------------------------------------------------------


# Installation
#### Firstly clone the yolov5 
``` !git clone https://github.com/ultralytics/yolov5 ```
#### In the same directory run the command to install the requirements
``` pip install -r requirements.txt```
#### Arrange the dataset in given order
##### dataset
* images <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; train <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; val
* labels <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; train <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; val

##### Divide the dataset in train and val folder. 
```
python3 arrange.py

```
#### Start training
```
python3 train.py --img 415 --batch 16 --epochs 30 --data /home/prince/Desktop/yolo/dataset.yaml --weights yolov5s.pt --cache

```
#### Detection
```
python3 detect.py --source runs/train/exp/a.jpg --weights best.pt
```
