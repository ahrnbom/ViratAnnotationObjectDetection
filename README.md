# ViratAnnotationObjectDetection
Object Detection-based annotations for some frames of the VIRAT dataset

The VIRAT dataset, available here http://www.viratdata.org/, is a large public dataset consisting of videos. Its original annotations are made from an event recognition standpoint, meaning that only objects that act in certain annotated events are annnotated. For training an object detector, such annotations are not very useful. The annotations provided in the repo on the other hand try to be useful from an object detection point of view.

Objects belonging to two classes have been annotated:
1. vulnerable road users (pedestrians, bikes, etc.) 
2. vehicles (cars, etc.) Note that parked cars are not annotated.

Not all frames have been annotated. Due to lack of time, it was chosen to only annotate 20 frames per video sequence (evenly spread out across the videos), and instead annotate as many sequences as possible. In total, 1260 frames have been annotated. A suggested split into a training and testing set is included.

The format for the annotations is as follows. Each folder corresponds to a video sequence from VIRAT Release 2. Inside each folder are a number of text files, called SEQNAME_FRAMENUMBER.txt. Inside each text file, each line corresponds to a single annotated object. The lines consist of object type (1 for vulnerable road user, 2 for vehicle), followed by the center coordinates of the box (x first, then y), followed by the width and height of the box. The boxes are axis-aligned and their coordinates are relative to the image size (so that a resized image can still be used). The values on the lines are separated by spaces.

The annotations provided here are free to use for any purpose (except claiming that you made them, unless you are me, who made them). These annotations are in no way an official part of the VIRAT dataset, and is not endorsed by or otherwise associated with the VIRAT dataset and its creators.   
