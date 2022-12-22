# Project Stop Lights

## Crosswalk Model

### Data Set and Preprocessing
We apdated the data set from the following Kaggle dataset:
https://www.kaggle.com/datasets/buvision/synthetic-crosswalks

We modified a script from the following repository to convert the data set to the XML format:
https://github.com/mhiyer/coco-annotations-to-xml

### Training
The crosswalk model was trained in the object-detection-api. We used the following resource for guideance in training our model:
https://catchzeng.medium.com/train-a-custom-object-detection-model-using-tensorflow-object-detection-api-7e49841f9bcb

### Evaluation
We wrote a jupyter notebook to evaluate the crosswalk model. We also evaulted the model using the testing data set.

### YoloV5
We used the YoloV5 model to detect the vehicles in the video. We used the following resource to help us integrate the YoloV5 model into our project:
https://github.com/ultralytics/yolov5

### Joint Application
We wrote a class which we intergrated into the YoloV5 model to keep track of the vehicles relative to the crosswalk. Running the following command within application to run the application:
```python3 track.py --source=../<SOME_VIDEO.mp4> --show-vid```