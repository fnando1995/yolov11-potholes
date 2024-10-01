# Pothole Segmentator in Road Images

## Description

This project focuses on training and utilizing a pothole segmentator for road images. By leveraging YOLOv11 nano, we perform image segmentation to accurately detect and measure potholes. The segmentation model is trained on a dataset that has been curated and processed to remove duplicate images, ensuring high-quality results.

## Installation
* Install Conda for managing the environment easily.
* Install PyTorch and Ultralytics:
```
conda install pytorch torchvision torchaudio -c pytorch
pip install ultralytics
```
* Install imagededup to eliminate duplicated images from the dataset:
```
pip install imagededup
```
Visit the official repository for more details: [imagededup](https://github.com/idealo/imagededup).


## Data Manipulation
* Some datasets were sourced from Roboflow.
* The datasets were cleaned and joined using imagededup to eliminate duplicate images. For further details, refer to the notebook image_similarity.ipynb.


## Training
* The training script uses the YOLOv11 nano model to perform pothole segmentation on road images.
* The dataset is defined via a YAML file for ease of configuration.
* At the end of training, the model is exported to ONNX format for compatibility with other platforms.

For detailed steps, refer to the notebook yolo11_train.ipynb.

## Inference
* A simple inference script is provided to test the trained model on a validation image.
* The inference script calculates the number of pixels occupied by potholes in the image.

For more information, see the notebook yolo11_infer_potholes.ipynb.