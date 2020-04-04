## Rice grain quality recognition project

### Resources:
tutorial: https://machinelearningmastery.com/how-to-train-an-object-detection-model-with-keras/

used labelme to label rice: https://github.com/wkentaro/labelme

### Dependencies:
matterport/Mask_RCNN: https://github.com/matterport/Mask_RCNN#installation
mask_rcnn doesn't work with tensorflow 2.0, using 1.14 for this project

### Setup:
python3 -m venv riceEnv

Define folder heiarchy as:
training/
- train_labels.csv
- imgs/
    - full.jpg
    - bad.jpg
- annots/
    - full.json
    - bad.json

### Problems:
- annotation points are in decimal places in json from labelme, don't know why, for time being going to cut off decimals.