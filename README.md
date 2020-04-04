## Rice grain quality recognition project

### Resources:
tutorial: https://machinelearningmastery.com/how-to-train-an-object-detection-model-with-keras/

used labelme to label rice: https://github.com/wkentaro/labelme

### Dependencies:
matterport/Mask_RCNN: https://github.com/matterport/Mask_RCNN#installation (this repo doesn't work with tensorflow 2.0, using 1.14 for this project)

### Setup:
`python3 -m venv riceEnv`
`source riceEnv/bin/activate`
`git clone https://github.com/matterport/Mask_RCNN`
`cd Mask_RCNN`
`pip install -r requirements.txt` (needs to downgrade tensorflow to 1.14)
`python setup.py install`

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

### Comments:
- Using bouding boxes instead of polygon in this dataset since the high contrast of rice and black background.