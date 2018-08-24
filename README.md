# Face Recognition for Identification #
This repository hosts my code for an image-based identification system. 

## Description ##
Images used in this demo are from the [MIT-CBCL face recognition database](http://cbcl.mit.edu/software-datasets/heisele/facerecognition-database.html). I use one of the two training sets this database contains: high-resolution face pictures (including frontal, half-profile and profile view) for each of the 10 subjects.

The test set consists of 200 lower-resolution images per subject, with varied illumination, pose, and background. I find the test photos a realistic simulation of the working environment of a real-world face-recognition-based user identification system. 

This system calls the `face_recogition` package by [Adam Geitgey](https://github.com/ageitgey). This package is based on an ImageNet model that was trained on only frontal view photos. This limit does not become a concern considering that the intended users of an identification system will always face the camera. 

With a tolerance of 0.6, the accuracy of this system is 0.9970 among all test photos. 

## Potential Future Work ##
One natural extension of this system is video-based identification. For such a task, `OpenCV` will be used to capture a single frame of video stream, and then the rest of the recognition process follows the same flow as in this demo. 

Other face recognition applications that are expected to capture people's face information from all angles other than frontal - such as security/monitoring system - will not benefit from the `face_recognition` package. We need to explore other methods such as Discrete Wavelet Transform. 

