# Developer - Winter of Code 2020
# Sourav Sharma
### Organisation Name : DocScanner

# Overview
 
## Project Overview
This project is aim at taking input image which may be in a different orientation and align this image.
This project was mentored and guided by - Rishiraj Acharya,Rajwrita,Ritesh.
 
 
## Contributions
 - Align image of pages #2: In this task, I was responsible for Align image of pages that are in different orientations using keypoint matching
 and a homography matrix so that we can apply OCR to the texts in the page.
 ## For this task i had taken the following steps
 ## Step 1:
  - Reading Image: First, we are going to take input using argparse and read it using opencv
  - Image preprocessing: This step includes converting our images to grayscale for edge detection
  - Edge Detection: Then we will carry out edge detection using canny edge detection.
 
 
 ## Step 2:
  - Finding Contours: First we will find contours of the image to get the cordinates of the edge of documents
  - Draw Bounding Box: Then we draw bounding box around our document for visualization purpose
  
 ## Step 3:
  - Four Points Transformation: First we will apply four points transformation to align our document
  - Gaussian Blur: Then we will apply gausian blur to give scanned effect on the document


 
 
## Language Used
 - Python
## Framework Used
 - Opencv
 - imutils
 - numpy
 - argparse
 



# New Features
 - Saving Resulting Output: Our script will save the the resulting output image as 'Scanned.png'


## Here is the link to my PR: [image_align_scan.py #6](https://github.com/dscnsec/DocScanner/pull/6) 

# Future Scope
 - I believe this project not only helps in document alignment but also opens up a new world of possiblities for DSC-NSEC. We can use this project as an advanced feature
 for document scanning in apps and many other.
 

# Overall Experience
- I had an enriching and exciting experience in winter of code,2020, working on DocScanner under DSC_NSEC. 
I was glad to be mentored by Rishiraj Acharya,Rajwrita,Ritesh(thanks for going through my PRs!). 
I express my sincere thanks to all students who worked on DocScanner
as part of WOC,2020.

