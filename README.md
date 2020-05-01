Prerequisites
This project is written in Python 3.7 using Tensorflow 2.0 (deep learning), NumPy (numerical computing), Pillow (image processing), OpenCV (computer vision) and seaborn (visualization) packages.

pip install -r requirements.txt


Using Custom trained weights

Add your custom weights file to weights folder and your custom .names file into data/labels folder.

Change 'n_classes=80' on line 97 of load_weights.py to 'n_classes=<number of classes in .names file>'.

Change './weights/yolov3.weights' on line 107 of load_weights.py to './weights/'.

Change './data/labels/coco.names' on line 25 of detection.py to './data/labels/'.

Save the weights in Tensorflow format
Load the weights using load_weights.py script. This will convert the yolov3 weights into TensorFlow .ckpt model files!

python load_weights.py

Running the model
You can run the model using detect.py script. The script works on images, video or your webcam. Don't forget to set the IoU (Intersection over Union) and confidence thresholds.

Usage
python detect.py <images/video/webcam> <iou threshold> <confidence threshold> <filenames>


python detect.py images 0.5 0.5 data/images/hat.jpg data/images/red_hat.jpg
