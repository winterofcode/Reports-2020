# Developer - Winter of Code 2020
# Abhinav Chauhan
### DSE NSEC : DocScanner

 The project was open-source mobile document scanner using computer vision. Mobile document scanners are a must-have for students and businesses for removing busy background and generating high resolution perfectly aligned images. My work over the winter made this happen solving the issue of aligning the image at realtime.

 I am [Abhinav Chauhan](http://github.com/Abhinav-2901), an undergraduate student from NIET, Greater Noida, as part of [Winter of Code](https://winterofcode.com/)

 This project was mentored by - [Rishiraj Acharya](https://github.com/rishiraj)

# Contributions
  ## There are Following Steps:-
### Reading image using OpenCV

### Image Preprocessing
* Converting orginal image to grey color
* Converting grey image to blurred image using Gaussian Blur
* Detecting edges using canny edge detector
* dilation and erosion of inage for better contour detection.

### Contour Detection
* He we handle all the contour Detected and keep only the one with the greatest contour area.
* After getting that contour we draw a bounding box around it for visualisation and keep the coordinates of the corners of the required contour detected.

### Wrapping the Image
* In this step we wrap the image with the ordered points i.e. (0,0) (width, 0) (0, height) and (width, height) which we got from the reorder function.

### Result Image
* Here we diplay the the final scanned image.

# Small Bugs
- [Align the image](https://github.com/dscnsec/DocScanner/issues/2)

Here are some of [my PRs](https://github.com/dscnsec/DocScanner/pull/5)

# Future Scope
* Working in the project of DocScanner not only we got more application in machine learning but we also got more intents towards different arean of computer vision.

# Overall Experience
* It was great exprience for me to got into Open Source culture through this great program and I would love to encorage more students to do this program in future.
