# Keras and Convolutional Neural Networks (CNNs)

# Dataset
Our deep learning dataset consists of 958 images of Pokemon. The Pokemon includes:
* Bulbasaur - 185 Images
* Charmander - 205 Images
* Mewtwo - 190 Images
* Pikachu - 191 Images
* Squirtle - 187 Images

The CNN architecture we will be utilizing today is a smaller, more compact variant of the VGGNet network, introduced by Simonyan and Zisserman in their 2014

VGGNet-like architectures are characterized by:
* Using only 3×3 convolutional layers stacked on top of each other in increasing depth
* Reducing volume size by max pooling
* Fully-connected layers at the end of the network prior to a softmax classifier

The file ```smallervggnet.py``` contains the smaller version of VGGNet model.

The file ```train.py``` will train the samller VGGNet on Dataset and save te model in a pickle file.
# Image Augmentation
Since we’re working with a limited amount of data points (< 250 images per class), we can make use of data augmentation during the training process to give our model more images (based on existing images) to train with.

The file ```classify.py``` is implemented to classify images that are not part of our training or validation/testing set.

# Output
