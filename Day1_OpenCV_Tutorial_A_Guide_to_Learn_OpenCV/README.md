# OpenCV Tutorial A Guide to Learn OpenCV

# Scripts

1) ***opencv_tutorial_01.py*** - Covers basic image processing operations using an image from the movie, Jurassic Park
2) ***opencv_tutorial_02.py*** - Shows how to use these image processing building blocks to create an OpenCV application to count the number of objects in a Tetris image

# Loading and displaying an image:

1) ***cv2.imread*** - Read or access the image
2) ***cv2.imshow*** - Display the image that is read

# Array slicing and cropping:

Extracting “regions of interest” (ROIs) is an important skill for image processing.
1) ***image[startY:endY, startX:endX]*** - Specifying the coordinates of the image we need to extract

# Resizing images:
1) ***cv2.resize*** - Resizing images as per our requirement or Resize a large image to fit on screen. (It ignores aspect ratio of images i.e. ratio of its width to its height)
2) ***imutils.resize*** - Resizing images as per our requirement as well as maintains the aspect ratio of the image.

# Rotating an image
1) ***cv2.getRotationMatrix2D*** - Rotate the image along the center point with the angle specified along with scaling options
2) ***cv2.warpAffine*** - Warp the image using the matrix (effectively rotating it).
3) ***imutils.rotate*** - Rotate the image along the center point with the angle specified and does not care whether the images is getting clipped or not. Usually not recommended as we may lose some important information.
4) ***imutils.rotate_bound*** - Rotate the image along the center point with the angle specified and also avoids clipping of the image.

# Smoothing an image
1) ***cv2.GaussianBlur*** - Blur an image to reduce high-frequency noise, making it easier for our algorithms to detect and understand the actual contents of the image rather than just noise that will “confuse” our algorithms.

# Drawing on an image
1) ***cv2.rectangle*** - Drawing a rectangle on an image
      1) `img` : The destination image to draw upon. We’re drawing on output.
      2) `pt1` : Our starting pixel coordinate which is the top-left. 
      3) `pt2` : The ending pixel — bottom-right. 
      4) `color` : BGR tuple. 
      5) `thickness` : Line thickness (a negative value will make a solid rectangle).
2) ***cv2.circle*** - Drawing a circle on an image
      1) `img` : The output image.
      2) `center` : Our circle’s center coordinate. 
      3) `radius` : The circle radius in pixels.
      4) `color` : Circle color. 
      5) `thickness` : The line thickness. 
3) ***cv2.line*** - Draws a line on an image
4) ***cv2.putText*** - Overlay text on an image for display purposes.
      1) `img` : The output image.
      2) `text` : The string of text we’d like to write/draw on the image.
      3) `pt` : The starting point for the text.
      4) `font` : Font of the text. I often use the cv2.FONT_HERSHEY_SIMPLEX 
      5) `scale` : Font size multiplier.
      6) `color` : Text color.
      7) `thickness` : The thickness of the stroke in pixels.

# Converting an image to grayscale
1) ***cv2.cvtColor*** - Converting image from BGR to Grayscale or vice versa

# Edge detection
1) ***cv2.Canny*** - Edge detection is useful for finding boundaries of objects in an image — It is effective for segmentation purposes.
      1) img : The gray image.
      2) minVal : A minimum threshold.  
      3) maxVal : The maximum threshold which is 150 in our example.
      4) aperture_size : The Sobel kernel size. By default this value is 3.

# Thresholding
1) ***cv2.threshold*** - Thresholding can help us to remove lighter or darker regions and contours of images.

# Detecting and drawing contours
1) ***cv2.findContours*** - To detect the contours(i.e., outlines) of the foreground objects in the image.
2) ***imutils.grab_contours*** - Grab to obtained contours
3) ***cv2.drawContours*** - Draw each contour on the output image

# Erosions and dilations
1) ***cv2.erode*** and ***cv2.dilate*** - Erosions and dilations are typically used to reduce noise in binary images (a side effect of thresholding).

# Masking and bitwise operations
1) ***cv2.bitwise_and*** - Masks allow us to “mask out” regions of an image we are uninterested in.
