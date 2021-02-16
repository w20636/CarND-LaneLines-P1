# **Finding Lane Lines on the Road** 

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 7 steps. 
#1 Converted the images to grayscale, 
#2 Applied Gaussian smoothing 
#3 Canny edge detection
#4 Region selection
#5 Run Hough transform
#6 Draw detected lines
#7 Combine with original image for display
In order to draw a single line on the left and right lanes, I modified the draw_lines() function by 
Calculate slope ratio and use it to extrapolate the 2nd point for display. I also tried to extrapolate 1st point. When I do that, I encountered resource overflow issue when processing the 27 sec video so I commented it out. 

The developed program was tested on the test images and test videos.


### 2. Identify potential shortcomings with your current pipeline
•	I found it is somewhat difficult to find optimal parameters for edge detection and hough transform. There might be better parameters to use than the ones I tested.
•	The region selection could be further optimized to filter out anything outside current driving lane.
•	Extrapolation of detected lines drawn could be further optimized.
•	There appears to be some random noises with Hough transform. I don’t quite understand why it is happening.


### 3. Suggest possible improvements to your pipeline

Improvements on shortcomings identified in step2.
