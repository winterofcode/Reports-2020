# Developer - Winter of Code 2020

# Piyush Thakur

### Deep Fusion AI : social-distance-detector

# Overview

In any pandemic where the disease is spread through physical contact, social distancing has always been the most efficient method to counteract the disease. So, in recent times where Covid-19 has devastated the lives of many, we need to maintain social distance among people. 

As a developer, we were handed a task to build a real-time social distancing detector with technologies like deep learning and computer vision and contribute something to counteract this devastating pandemic.

I am **Piyush Thakur**, an undergraduate student from **NSEC**, **Kolkata**, as part of **Winter of Code 2020**.

This project was mentored by **Sayak Paul** bhaiya and **Rishiraj Acharya** bhaiya.

# Contributions

## Issue [#5](https://github.com/DeepFusionAI/social-distance-detector/issues/5) 

### Deliverables

* The TensorFlow Lite model
* A Colab Notebook showing the model conversion process and how to make predictions with the TensorFlow Lite model on static images

### My Contributions for this issue

Here is my [colab](https://colab.research.google.com/drive/16Eq2_ajBd-7xGdmXG4aKgnlN3yFnx1pK?usp=sharing) showing all my **completed work** for this issue.

* I have used **SSD_mobileDet_cpu_coco*** as a pretrained model.
* I have used the **checkpoint of this pretrained model** and converted it into **TensorFlow Lite compatible model graph**.
* I quantized the **TensorFlow Lite compatible model graph** into **TensorFlow Lite model**.
* I have included **three variants** of this model : **SSD_mobileDet_cpu_coco_int8, SSD_mobileDet_cpu_coco_fp16, SSD_mobileDet_cpu_coco_dr**.
* I have made a Representative dataset by downloading **COCO train2014 annotations** and **subsampling 200 images for person only** which I later used it for quantization.
* Finally, I have used these **model variants to detect only pedestrians in a static image**.

***Note - At final process, the processing of the image, loading of the COCO labels containing only person class was also done.***

###### Model Benchmark

|Model Name|Model Size(MB)|Elapsed Time(s)|
|--- |--- |--- |
|SSD_mobileDet_cpu_coco_int8|4.9|1223.54|
|SSD_mobileDet_cpu_coco_fp16|8.2|83.92|
|SSD_mobileDet_cpu_coco_dr|4.9|1240.47|

As we can see from the **Model Benchmark** table shown above, I have shown the **model variants size** and **elapsed time** taken to detect the pedestrians in a static image.

***Note - The fp16 variant of SSD_mobileDet_cpu_coco is the fastest and the most accurate model which detected the pedestrians in a shortest time possible, that is 83.92 milliseconds.***

## Issue [#4](https://github.com/DeepFusionAI/social-distance-detector/issues/4)

### Considerations

* As the detector would be running on real-time video feeds using TensorFlow Lite with Python on a Raspberry Pi 4 Model B, you should focus on the latency aspects of it without compensating for its accuracy. An ideal model would be fast and at the same time won't produce too many false positives. Also, consider if the detector should run on every single frame of a video feed, or could we minimize it?

* As you would try out different models for the purpose please do a thorough study of their latency along with their detection performance on videos. This information will make it easier for us to decide which model we might want to go with.

### Deliverables

* A Colab Notebook to demonstrate the idea.
* A Python script (you can modularize code with multiple scripts too) for the end-to-end execution i.e. this script will take real-time video feeds as its input from a Pi Camera, detect pedestrians, and will display the results on the screen.

### My Contributions for this issue

Here is my [colab](https://colab.research.google.com/drive/1HczCWXwnaqU1uZ9rGxnxL4JWVE7rmjCo?usp=sharing) showing all my **completed work** for this issue.

* I have used the same model variants, that is **SSD_mobileDet_cpu_coco** for this issue as mentioned before.
* I have used the same strategies for **model conversion** as mentioned before.
* I have used the same **Representative Dataset** for this issue as mentioned before.
* Finally, I have used these **model variants to detect only pedestrians in a video**.

***Note - At final process, the processing of each frame of video, loading of the COCO labels containing only person class was also done.***

###### Model Benchmarks

|Model Name|Model Size(MB)|Elapsed Time(s)|FPS|
|--- |--- |--- |--- |
|SSD_mobileDet_cpu_coco_int8|4.9|705.32|0.75|
|SSD_mobileDet_cpu_coco_fp16|8.2|52.79|10.06|
|SSD_mobileDet_cpu_coco_dr|4.9|708.57|0.75|

As we can see from the **Model Benchmark** table shown above, I have shown the **model variants size**, **elapsed time**, and **FPS(Frame per second)** of all the three variants of the **SSD_mobileDet_cpu_coco** model.

***Note - The fp16 variant of SSD_mobileDet_cpu_coco is the fastest and the most accurate model, giving a whooping FPS of 10.06.***

As the model will be used for social distancing detection in real-time, the use of **SSD_mobileDet_cpu_coco_fp16** is the best one to pick and mentors also agreed to it.

###### Results

Here is the ![video](https://github.com/piyush-cosmo/WoC_sdd_test/blob/master/pedestrian_detection/pedestrian_detected.mp4) showing the result.

## Fun experiment with TensorFlow Lite Benchmark Tool given by mentors 

### My Contributions

Here is the image ![image](https://github.com/piyush-cosmo/WoC_sdd_test/blob/master/pedestrian_detection/Annotation%202020-12-29%20190820.png) showing the result.

* I have configured **Android Debug Bridge(adb)** in my laptop and connected it with my android device to use **TensorFlow Lite Benchmark Tool** to check the **Inference speed** of the best model, that is **SSD_mobileDet_cpu_coco_fp16** model. 
* The first result in the image given above is with the use of **cpu with 4 threads**.
* The second result in the image given above is with the use of **gpu**.

## Final integration in colab to complete the project

As **SSD_mobileDet_cpu_coco_fp16** produced so good results, mentors instructed us to incorporate this model into the whole pipeline.

### My Contributions

I helped in integrating mobileDet model into the complete pipeline. Here is my [colab](https://colab.research.google.com/drive/1FbXD9kMwmTE3UW56H41QlWMiNQtZ6Irp?usp=sharing) showing the **completed work** for this issue.

###### Results

Here is the ![video](https://github.com/DeepFusionAI/social-distance-detector/blob/master/videos/Detailed_output.mp4) showing the result.

## Code Modularisation

Finally, I also helped in code modularization. Here is my [PR](https://github.com/DeepFusionAI/social-distance-detector/pull/9) showing my work.

# New Features

As this project started from the beginning, all the things added are the new features.

# Small Bugs

The project is completed, there is no bugs in the project.

# Future Scope

We can implement this real-time social distancing detection model to places like colleges and malls, places where crowd gathers and can regulate the masses so that the spread of coronavirus can be maintained and monitored.

* We can install Raspi cameras at these places, calibrate it according to the place and detect the person in real-time. When person distance gets below 6 feet, the system emits a non-alarming audio-video cue.

# Overall Experience

It was really a great experience since this 1 month of Winter of Code, learned a lot from mentors. We were actually blessed with the mentors, being so knowledgable and down-to-earth persons. Their support and guidance made this project a complete one. The peers(**Sudarshana**, **Subhasmita**, **Hiran**) were great too, I enjoyed bonding and working with them. I loved the entire journey.
