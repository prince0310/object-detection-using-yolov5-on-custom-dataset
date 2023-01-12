# object-detection-using-yolov5-on-custom-dataset
I have implemented yolov5 on custom dataset

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
python detect.py --source runs/train/exp/a.jpg --weights best.pt
```
