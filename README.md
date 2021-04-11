# Drowsiness Detection System
Drowsiness detection is a safety technology that can prevent accidents that are caused by drivers who fell asleep while driving. The system that will detect that a person’s 
eyes are closed for a few seconds. This system will alert the driver when drowsiness is detected.


## Description
This program is used to detect drowsiness for any given person. In this program we check how long a person's eyes have been closed for. If the eyes have been closed for a 
long period i.e. beyond a certain threshold value, the program will alert the user by playing an alarm sound.

## Requirements
Download shape_predictor_68_face_landmarks.dat.bz2 from [Shape Predictor 68 features](http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2) Extract the file in 
the project folder using 
  ``bzip2 -dk shape_predictor_68_face_landmarks.dat.bz2``


### Dependencies
1. import numpy
2. import dlib
3. import pygame
4. import imutils
5. import opencv_python
6. import scipy 

## Algorithim
* Each eye is represented by 6 (x, y)-coordinates, starting at the left-corner of the eye (as if you were looking at the person), and then working clockwise around the eye

* Now that we have the eye regions, we can compute the eye aspect ratio to determine if the eyes are closed or not.

* If the eye aspect ratio falls below the threshold, we’ll start counting the number of frames the person has closed their eyes for.

* If the number of frames the person has closed their eyes in exceeds EYE_AR_CONSEC_FRAMES, we’ll sound an alarm.


## Execution

Run script using:
```
python drowsinessDetection.py
```
