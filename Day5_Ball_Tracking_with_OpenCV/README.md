# Ball Tracking with OpenCV

# 2 Key Steps
1) Detect the presence of a colored ball using computer vision techniques.
2) Track the ball as it moves around in the video frames, drawing its previous positions as it moves.

# Packages to be used
1) ***deque*** - A list-like data structure with super fast appends and pops to maintain a list of the past N (x, y)-locations of the ball in our video stream. 

# OpenCV commands used:
1) ***cv2.cvtColor*** - Converting image from BGR to Grayscale or vice versa
2) ***cv2.GaussianBlur*** - Blur an image to reduce high-frequency noise, making it easier for our algorithms to detect and understand the actual contents of the image rather than just noise that will “confuse” our algorithms.
3) ***cv2.inRange*** - Handles the actual localization of the ball.
4) ***cv2.erode*** and ***cv2.dilate*** - Erosions and dilations are typically used to reduce noise in binary images (a side effect of thresholding).
5) ***cv2.findContours*** - To detect the contours(i.e., outlines) of the foreground objects in the image.
6) ***imutils.grab_contours*** - Grab to obtained contours
7) ***cv2.minEnclosingCircle*** - It is a circle which completely covers the object with minimum area i.e. To ensure that the radius of the minimum enclosing circle is sufficiently large.
8) ***cv2.moments*** - Moments are used to describe several properties of an image, such as the intensity of an image, its centroid, the area, and information about its orientation.
9) ***cv2.line*** - Draws a line on an image
