# Document Scanner with OpenCV

# 3 Key Steps:
1) Detect edges.
2) Use the edges in the image to find the contour (outline) representing the piece of paper being scanned.
3) Apply a perspective transform to obtain the top-down view of the document.

# OpenCV commands used:
1) ***cv2.getPerspectiveTransform*** - A perspective transform is used to obtain a top-down, “birds eye view” of an image — provided that we could find reference points.
2) ***cv2.warpPerspective*** - Warped or Top-Down view of the image.

