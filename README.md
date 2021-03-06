# Motion-Detector-Using-Python-Opencv
This python program will allow you to detect any motion that occurs in front of the builtin webcam and also store the time interval of the motions while creating a plot of the time interval using Bokeh Plot.

#### Requirement:
1. Python3
2. OpenCV(libraries)
3. Pandas(libraries)

Install Requirments: Install Python3, install Pandas and OpenCV libraries.

#### Main Logic: 
Videos can be treated as stack of pictures called frames. Here i am comparing different frames(pictures) to the first frame which should be static(No movements initially). We compare two images by comparing the intensity value of each pixels.

#### Analysis of all windows
After running the code there 4 new window will appear on screen. Output of each frame is added in this repository.

1. Gray Frame: In Gray frame the image is a bit blur and in grayscale we did so because, In gray pictures there is only one intensity value whereas in RGB(Red, Green and Blue) image thre are three intensity values. So it would be easy to calculate the intensity difference in grayscale.

2. Difference Frame: Difference frame shows the difference of intensities of first frame to the current frame.

3. Threshold Frame: If the intensity difference for a particular pixel is more than 30(in my code) then that pixel will be white and if the difference is less than 30 that pixel will be black.

4. Color Frame: In this frame you can see the color images in color frame along with green contour around the moving objects.

#### Time Record of movements

The Time_of_movements file will be stored in the folder where your code file is stored. This file will be in csv extension. In this file the start time of motion and the end time of motion will be recorded. 

#### Plotting Time Intervals
Time Intervals will be plotted using Bokeh Plot. Bokeh is an interactive visualization library that targets modern web browsers for presentation. Here, the time intervals are collected by the csv file and then plotted using Bokeh. The green color shows that an object was under motion, time is displayed in milisecond(ms). a screenshot of output is added in this repository.





----------------------------------------------------------------------------------------------------------------------------------------

##### There are 2 Python(.py) Files and 1 Jupyter Notebook(.ipynb) file present in this Repository 
###### motion_detector.py : Conatins the main code for motion detection without plotting the Bokeh Plot. 
###### plotting.py : Run this file for Bokeh plot (Imp. motion_detector.py file is needed in same directory for this file to run)
###### motion_detector.ipynb : This is Jupyter Notebook File code.
