# Sign-Language-Recognition
Sign language recognition model using [Detectron2](https://github.com/facebookresearch/detectron2) Object Detection Model. It is language agnostic and allows sign language recognition on static images. Here Faster RCNN model is used for transfer learning. Other models can be selected based on requirements and preference from the [model ZOO](https://github.com/facebookresearch/detectron2/blob/master/MODEL_ZOO.md).

Run this notebook directly on colab.

## Configurations
* `DATASET_URL`- URL of dataset hosted online. 
* `LABELS` - Number of labels you want to identify + 1. Eg- If you have 10 signs then `LABELS=11`                        
* `THRESHOLD` - Threshold value of confidence on identified label. If confidence is below threshold, no labels are shown. Value lies in `[0,1]`. 

## Steps
#### Create dataset
Decide on number of signs you want the model to detect. For each sign take multiple photos and label them in YOLO format. You can use any labling tool available online. I have used [LabelImg](https://github.com/heartexlabs/labelImg) to create the labels.
Put all the label files inside the same folder as images. Dataset is created.
#### Convert dataset into COCO format
Detectron2 requires dataset in COCO format. Various tools online are available to convert YOLO into COCO format. I have used [Roblflow](https://roboflow.com/) for this. It also provides you to host the dataset online which can be download through URL, it will be useful if you want to run the model on colab, as a direct link to dataset would be available.
#### Installations
- numpy and cv(colab come with this already installed)
`pip install numpy`
`pip install opencv-python`

Other installations are provided in notebook itself


