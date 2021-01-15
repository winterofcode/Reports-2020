# Developer - Winter of Code 2020

# **Sudarshana Dutta**


### **Deep Fusion AI : Social Distance Detector**

In any pandemic where the disease spreads through physical contact, social distancing has always been the most efficient method to counteract the disease. So, in recent times where Covid-19 has devastated the lives of many people, we need to maintain social distance among people. A majority of industries are demanding a tool to determine the extent to which people are following this safety protocol.


My work over the winter helped the team to successfully build a [real-time social distance detector](https://github.com/DeepFusionAI/social-distance-detector), which is fast and accurate enough to run inference on real-time video-feed. It uses a TensorFlow Lite pretrained model (SSD_mobileDet_cpu_coco) which is a light-weight model with low latency, high inference speed and much higher accuracy, with Python on a Raspberry Pi 4 Model B. It is implemented as such it is feasible for commercial use and can be converted to an open source software package.


Introducing myself, I am [Sudarshana Dutta](https://www.linkedin.com/in/sudarshanadutta2018/), an undergraduate student pursuing B. Tech in Computer Science Engineering (CSE) from [IEM](https://iem.edu.in/), Kolkata.


This project was mentored by [Rishiraj Acharya](https://www.linkedin.com/in/rishirajacharya/) and [Sayak Paul](https://github.com/sayakpaul). It is because of their constant guidance and motivation that made this project successful.


# Contributions

[61 Commits](https://github.com/DeepFusionAI/social-distance-detector/commits/master)


I primarily worked upon the [issue 6](https://github.com/DeepFusionAI/social-distance-detector/issues/6) assigned to me, which deals with:

### 1. Pedestrian Detection

Using the SSD_mobileDet_cpu_coco object detection model suggested by the mentors, only pedestrians are detected from the input image frames.
The detection procedure involves selecting the outcomes with sufficient confidence, locating the position, and determining the coordinates for bounding boxes around the predicted people.

Check the task [here](https://github.com/DeepFusionAI/social-distance-detector/blob/master/deepfusionai/pedestrian_detection.py).


Mentors and peers have helped me a lot to work with the model, which was new to me, and I've learnt a lot of many new features about the tools and models used.


### 2. Calibration

Each frame will have an arbitrary perspective view, which causes difficulty to analyse or calculate uniformly the relative distance between the people. So, it’s necessary to convert the frame view into a bird's eye (top-down) view. This process is termed as calibration. This ensures that everyone is on the same flat ground plane.
Check the task [here](https://github.com/DeepFusionAI/social-distance-detector/blob/master/deepfusionai/social_distance_detection.py).


### 3. Determining Social Distance Violation

After having positions of people in the top-down view, the final step of pipeline is to check if any person is in close proximity to one or more people.
An average person height is 5-6 feets. And we need to maintain social distance of 6 feets. Thus, from the results of pedestrian detector, the median height of people is determined, and we set this height as social-distance-violation parameter.
Check the task [here](https://github.com/DeepFusionAI/social-distance-detector/blob/master/deepfusionai/pedestrian_detection.py).


### 4. Visualisation

Everything is useless without visualising what's happening!


Based on what mentors planned, the project shows 3 frames to show results. In our project, colour "green" symbolizes people following social distancing and colour "red" remarks people violating the safety norm.
Check the task [here](https://github.com/DeepFusionAI/social-distance-detector/blob/master/deepfusionai/pedestrian_detection.py).
Visualise the videos [here](https://github.com/DeepFusionAI/social-distance-detector/tree/master/videos).


### 5. Inference

All the functionalities are integrated together to work upon and act accordingly :

- Load a TFLite model
- Load input video
- Process the video as a series of frames
- Pre-process each frame
- Running the inference
- Show and save the output video


Here are some of [my PRs](https://github.com/DeepFusionAI/social-distance-detector/pull/8)

My complete work is described in this [colab](https://github.com/DeepFusionAI/social-distance-detector/blob/master/WOC_pedestrian_detector_SD.ipynb).


# New Features

The social-distance detector add bounding boxes on the people - those violating the norm have red boxes and others have green boxes. In addition to this, the detector
- draws lines connecting all the pairs in close proximity.
- shows the count of people violating the social-distancing norm.
- predict the total number of frames in the video.
- shows the input video in bird's eye view frame as well.
- shows a black grid, which clearly demonstrates the detector's functioning - red and green points depicting people on a black background in top-down view with red connecting lines between the violators.

# Future Scope

I believe my contribution has helped to develop the project successfully and solve some important issues. But, it has opened up many new avenues. This project can be definitely improved by adding or updating one or more features, some of which are as follows :

- Current FPS is 8.97, which is really very good for real-time operations. Detection scores and FPS can be further improved with improved training and models.


- We have assumed that the camera position is fixed at a position. So, the detector is working on all video frames based on a specific top-down transformation matrix processed on a single frame. This can be improved by working upon transformations on all video frames without compromising with the speed and FPS of the detector.


- For calibration, the 4 corners of the rectangle are set using a user-interactive mouse-click event. In future, we can work upon finding a suitable rectangle from frame automatically by training such detection models or finding a tool to accomplish this task. This will also allow to calibrate images on every frame.

- In case the input video is too large (or to speed up the processing further), the detector can be allowed to process frames in an interval and skip some in the middle, only if it doesn't affect the performance.


# Overall Experience

I had a great experience working in [Winter of Code 2020](https://winterofcode.com/). This project matched my interests and further enriched my knowledge and skills. I am glad that I applied my ideas and developed something new. I want to thank the mentors - Rishiraj and Sayak - for supporting me throughout the session. I express my gratitude to my peers - [Piyush Thakur](https://github.com/piyush-cosmo), [Subhasmita Swain](https://github.com/SubhasmitaSw), and [Hiran Sarkar](https://github.com/around-star) - who made a great team.
Thanks NSEC for orgainising this event. Cheers!
