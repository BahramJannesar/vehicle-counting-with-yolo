## What is YOLO ?
YOLO is an abbreviation for the term 'You Only Look Once'. This is an algorithm that detects and recognizes various objects in a picture (in real-time). Object detection in YOLO is done as a regression problem and provides the class probabilities of the detected images.

## How this project works ?

Attach a video file to the project and the YOLO algorithm start to counting vehicles, i used coco name dataset for tags.
Check this [link](https://drive.google.com/file/d/1BpGvY9Y6Rja6wGJHiANwXlhno3XDw-5b/view?usp=sharing) for sample of this project

## Prerequisites

1. Linux distro
2. A street video file to run the vehicle counting
3. The pre-trained yolov3 weight file should be downloaded:

    ``cd yolo-coco``
    
    ``wget https://pjreddie.com/media/files/yolov3.weights``

## Dependencies 

First of all ,making a virtualenv from these steps:

    pip install virtualenv
    virtualenv venv
    source venv/bin/activate
    
After these steps installing pakages you need for project:

    pip install -r requirement.txt
    

## How to run project ?

* `--input` or `-i` argument requires the path to the input video
* `--output` or `-o` argument requires the path to the output video
* `--yolo` or `-y` argument requires the path to the folder where the configuration file, weights and the coco.names file is stored
* `--confidence` or `-c` is an optional argument which requires a float number between 0 to 1 denoting the minimum confidence of detections. By default, the confidence is 0.5 (50%).
* `--threshold` or `-t` is an optional argument which requires a float number between 0 to 1 denoting the threshold when applying non-maxima suppression. By default, the threshold is 0.3 (30%).
* `--use-gpu` or `-u` is an optional argument which requires 0 or 1 denoting the use of GPU. By default, the CPU is used for computations
```
python3 yolo_video.py --input <input video path> --output <output video path> --yolo yolo-coco [--confidence <float number between 0 and 1>] [--threshold <float number between 0 and 1>] [--use-gpu 1]
```

