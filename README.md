## TAD - 2.0

The purpose of this project is to detect and track vehicles on a video stream and count those going through a defined ROI

## It uses:

- [YOLO](https://www.pyimagesearch.com/2018/11/12/yolo-object-detection-with-opencv) to detect objects on each of the video frames.

- [SORT](https://github.com/abewley/sort) to track those objects over different frames.

Once the objects are detected and tracked over different frames a simple mathematical calculation is applied to count the intersections between the vehicles previous and current frame positions with a defined line.

## Dependencies

    python
    numpy
    opencv 3
    tensorflow 1.0

## Quick Start

1. Download the code to your computer.

2. [Download yolov3.weights](https://www.dropbox.com/s/99mm7olr1ohtjbq/yolov3.weights?dl=0) and place it in `/yolo-coco`.

3. Make sure you have Python 3.7.0 and [OpenCV 3.4.2](https://www.pyimagesearch.com/opencv-tutorials-resources-guides/) installed.

4. Run:

```
$ python main.py --input input/highway.mp4 --output output/highway.avi --yolo yolo-coco
```

5. Output frames are places in Output folder and final video file is created once the execution completes

6. Use dedicated GPU for faster processing.

## Citation

### Yolov3 :

    @article{redmon2016yolo9000,
      title={YOLO9000: Better, Faster, Stronger},
      author={Redmon, Joseph and Farhadi, Ali},
      journal={arXiv preprint arXiv:1612.08242},
      year={2016}
    }

### Sort :

    @inproceedings{Bewley2016_sort,
      author={Bewley, Alex and Ge, Zongyuan and Ott, Lionel and Ramos, Fabio and Upcroft, Ben},
      booktitle={2016 IEEE International Conference on Image Processing (ICIP)},
      title={Simple online and realtime tracking},
      year={2016},
      pages={3464-3468},
      keywords={Benchmark testing;Complexity theory;Detectors;Kalman filters;Target tracking;Visualization;Computer Vision;Data Association;Detection;Multiple Object Tracking},
      doi={10.1109/ICIP.2016.7533003}
    }
