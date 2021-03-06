# Real-time object detection with deep learning and OpenCV

To build deep learning-based real-time object detector with OpenCV we’ll need to 
1) Access our webcam/video stream in an efficient manner 
2) Apply object detection to each frame.

# OpenCV commands used:

1) ***cv2.dnn.readNetFromCaffe*** - Read the caffe protxt file and model file
2) ***cv2.dnn.blobFromImage(image, scalefactor=1.0, size, mean, swapRB=True)*** -Takes care of pre-processing which includes setting the blob dimensions and normalization.
 Parameters Used:
    1) `image` : This is the input image we want to preprocess before passing it through our deep neural network for classification.
    2) `scalefactor` : After we perform mean subtraction we can optionally scale our images by some factor. This value defaults to `1.0 (i.e., no scaling)` but we can supply another value as well. It’s also important to note that scalefactor should be 1 / σ as we’re actually multiplying the input channels (after mean subtraction) by scalefactor .
    3) `size` : Here we supply the spatial size that the Convolutional Neural Network expects. For most current state-of-the-art neural networks this is either 224×224, 227×227, or 299×299.
    4) `mean` : These are our mean subtraction values. They can be a 3-tuple of the RGB means or they can be a single value in which case the supplied value is subtracted from every channel of the image. If you’re performing mean subtraction, ensure you supply the 3-tuple in `(R, G, B)` order, especially when utilizing the default behavior of swapRB=True .
    5) `swapRB` : OpenCV assumes images are in BGR channel order; however, the mean value assumes we are using RGB order. To resolve this discrepancy we can swap the R and B channels in image by setting this value to `True`. By default OpenCV performs this channel swapping for us.

# Execution Command:
python real_time_object_detection.py --prototxt MobileNetSSD_deploy.prototxt.txt --model MobileNetSSD_deploy.caffemodel

# Output:
<table>
  <tr>
     <td> <h3>AEROPLANE PREDICTIONS</h3> </td>
     <td> <h3>HORSE AND PERSON PRECTIONS</h3> </td>
  </tr>
  <tr>
    <td> <img src="images/aeroplane_predicted.png"  alt="1" width = 600px height = 480px ></td>
    <td><img src="images/horse_predicted.png" alt="2" width = 600px height = 480px></td>
   </tr> 
</table>
