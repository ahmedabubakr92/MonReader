# MonReader

MonReader is a new mobile document digitalization experience for the blind, for researchers and for everyone else in need for fully automatic, highly fast and high-quality document scanning in bulk. It is composed of a mobile app and all the user needs to do is flip pages and everything is handled by MonReader: it detects page flips from low-resolution camera preview and takes a high-resolution picture of the document, recognizing its corners and crops it accordingly, and it dewarps the cropped document to obtain a bird's eye view, sharpens the contrast between the text and the background and finally recognizes the text with formatting kept intact, being further corrected by MonReader's ML powered redactor.

We collected page flipping video from smart phones and labelled them as flipping and not flipping.

We clipped the videos as short videos and labelled them as flipping or not flipping. The extracted frames are then saved to disk in a sequential order with the following naming structure: VideoID_FrameNumber.

The objective is to predict if the page is being flipped using a single image.

I've started by loading the data into two separate datasets of training and testing. Then, I've resized and rescaled the images for it to be in a lower-dimension which leads to simpler modeling and computation. At last, I've created a custom Convolutional Neural Network (CNN) model and applied it to the data and it yielded the following:
- The accuracy of the model on the training data: 0.9992
- The accuracy of the model on the testing data: 0.9950
- The F1-Score of the model on the training data: 0.9992
- The F1-Score of the model on the testing data: 0.9949
