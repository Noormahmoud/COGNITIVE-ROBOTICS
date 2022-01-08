# COGNITIVE-ROBOTICS
Reading and displaying an image using the Python-OpenCV interface

we will load an image in grayscale and display it on screen

install the OpenCV :

```
$ sudo apt-get install python-opencv
```

In the following section of code, we will import the numpy module for image array manipulation and the cv2 module is the OpenCV wrapper for Python in which we can access OpenCV Python APIs.
```
import numpy as np
import cv2
```
The following function will read the `flower.jpg` image and load this image in grayscale. The first argument of the `cv2.imread()` function is the name of the  image and the next argument is a flag that specifies the color type of the loaded image. If the flag is > 0, the image returns a three channel RGB color image, if the  flag = 0, the loaded image will be a grayscale image, and if the flag is < 0, it will return the same image as loaded:

```
img = cv2.imread('flower.jpg',0)
```
The following section of code will show the read image using the `imshow() function`. The `cv2.waitKey(0)` function is a keyboard binding function. Its argument is time in milliseconds. If it's 0, it will wait indefinitely for a key stroke:
```
cv2.imshow('image',img)
cv2.waitKey(0)
```
The `cv2.destroyAllWindows()` function simply destroys all the windows we created:
```
cv2.destroyAllWindows()
```
Save the preceding code with a name called `img_read.py` and copy a JPG file with `flower.jpg` as its name
Execute the code using the following command:
```
$ python img_read.py
```
The output will load an image in grayscale because we used 0 as the value in the `imread()` function:

<img src = "https://raw.githubusercontent.com/Noormahmoud/COGNITIVE-ROBOTICS/main/flower%20in%20grayscale%20.png">
