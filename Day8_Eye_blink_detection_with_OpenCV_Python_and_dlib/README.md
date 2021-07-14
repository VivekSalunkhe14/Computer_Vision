# Eye blink detection with OpenCV, Python, and dlib

To build Eye blink detector, we’ll be computing a metric called the eye aspect ratio (EAR). The eye aspect ratio is instead a much more elegant solution that involves a very simple calculation based on the ratio of distances between facial landmarks of the eyes.

# 3 Key Steps:
1) Compute Eye Aspect Ratio
2) Perform facial landmark detection and detect blinks in video streams.
3) Apply method to detecting blinks in example webcam streams along with video files.

# OpenCV commands used:
1) ***cv2.cvtColor*** - Converting image from BGR to Grayscale or vice versa
2) ***cv2.rectangle*** - Drawing a rectangle on an image
3) ***cv2.circle*** - Drawing a circle on an image
4) ***cv2.convexHull*** - Identify the convex hull 

NOTE: The dlib shape detector file "shape_predictor_68_face_landmarks.dat" is not uploaded in this directory since it is too big. Please download this file and position in the same folder for execution of this project.
