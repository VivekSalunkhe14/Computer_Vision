# Facial landmarks with dlib, OpenCV, and Python

Facial landmarks are used to localize and represent salient regions of the face, such as:
* Mouth
* Right eyebrow
* Left eyebrow
* Right eye
* Left eye
* Nose
* Jaw

Facial landmarks have been successfully applied to face alignment, head pose estimation, face swapping, blink detection and much more.

The pre-trained facial landmark detector inside the dlib library is used to estimate the location of 68 (x, y)-coordinates that map to facial structures on the face.

# 2 Key Steps:
1) Localize the face in the image.
2) Detect the key facial structures on the face ROI.

# OpenCV commands used:
1) ***cv2.cvtColor*** - Converting image from BGR to Grayscale or vice versa
2) ***cv2.rectangle*** - Drawing a rectangle on an image
3) ***cv2.circle*** - Drawing a circle on an image

# Output
<table>
  <tr>
     <td> <h3>ORIGINAL IMAGE</h3> </td>
     <td> <h3>FACIAL LANDMARK IMAGE</h3> </td>
  </tr>
  <tr>
    <td> <img src="multiplefaces.jpg"  alt="1" width = 768 height = 1024px ></td>
    <td><img src="face_landmark.png" alt="2" width = 768px height = 1024px></td>
   </tr> 
</table>
