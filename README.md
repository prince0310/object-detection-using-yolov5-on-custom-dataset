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
 
 
    !git clone https://github.com/ultralytics/yolov5
 
 ### Install the required packages:
 
    pip install -r requirements.txt 
    
 
 ### Download the YOLOv5 weights from the official [website](https://github.com/ultralytics/yolov5) and place them in the weights directory.
 
# Dataset

The dataset should be in the format of PASCAL VOC and should be placed in the data directory. The dataset should have following structure:

data<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  train..<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;    images.. <imagename>.jpg<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  annotations.. <imagename>.xml<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  val <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;    images.. <imagename>.jpg<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   annotations.. <imagename>.xml<br>

# Training
To train the model, run the following command: 


     python train.py --data <path to data file> --cfg <path to config file> --weights <path to weights file> --batch-size <batch size> --epochs <number of epochs>

> * Note: You can also use the --img-size flag to set the input image size and the --img-weights flag to specify the weight file of the model.

# Model Inference

##### After the training is complete, you will have a trained model in the weights folder.
 Use the command to test the model on a single image or video.
   
    python detect.py --weights <path to weight file> --source <path to image/video file> --conf-thres <confidence threshold> --iou-thres <IoU threshold>
    
 
 # Conclusion

This guide has provided an overview of how to train a YOLOv5 model on a custom dataset for object detection. With a trained model, you can now use the model to perform object detection on new images and videos. Keep in mind that the accuracy of the model will depend on the quality of the dataset and the amount of training data used.
    
    
