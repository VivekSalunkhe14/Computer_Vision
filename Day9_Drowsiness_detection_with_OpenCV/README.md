# Drowsiness detection with OpenCV

# 3 Key Steps:
1) Setup video camera to easily detect face and apply facial landmark localization to monitor my eyes.
2) Demonstrate how to can implement drowsiness detector using OpenCV, dlib, and Python.
3) Alert the driver by ringing an alarm in case if he is asleep while driving.

# OpenCV commands used:
1) ***cv2.cvtColor*** - Converting image from BGR to Grayscale or vice versa
2) ***cv2.rectangle*** - Drawing a rectangle on an image
3) ***cv2.circle*** - Drawing a circle on an image
4) ***cv2.convexHull*** - Identify the convex hull 

# Execution Command:
python detect_drowsiness.py --shape-predictor shape_predictor_68_face_landmarks.dat --alarm alarm.wav
