# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read two images, Color image and Gray Scale image.

### Step2:
Calculate the Histogram of Gray scale image and each channel of the color image.

### Step3:
Display the histograms with their respective images.

### Step4:
Equalize the grayscale image.

### Step5:
Display the grayscale image.

## Program:
```python
# Developed By:DHANASHREE M
# Register Number:212221230018
import cv2
import matplotlib.pyplot as plt

# Write your code to find the histogram of gray scale image and color image channels.
import cv2
import matplotlib.pyplot as plt
Gray_image = cv2.imread("gray.jpg")
cv2.imshow("Gray Image",Gray_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

import cv2
import matplotlib.pyplot as plt
Color_image = cv2.imread("clrr.jpg")
cv2.imshow("Colour_image",Color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()




# Display the histogram of gray scale image and any one channel histogram from color image
import numpy as np
import cv2
Gray_image = cv2.imread("gray.jpg")
Color_image = cv2.imread("clrr.jpg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
cv2.destroyAllWindows()




# Write the code to perform histogram equalization of the image. 
import cv2
gray_image = cv2.imread("gray.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image
![Screenshot 2023-04-05 212052](https://user-images.githubusercontent.com/94165415/230136736-6d2d600d-b922-455f-9366-e028437d1329.png)

### Histogram of Grayscale Image and any channel of Color Image
![hist dip1](https://user-images.githubusercontent.com/94165415/230137228-b9010e75-db1f-432f-9795-3e6b4d9e65d4.png)
![hist dip11](https://user-images.githubusercontent.com/94165415/230137316-8ee9b39a-cf35-4f80-afe8-d3ecb0804e1b.png)


### Histogram Equalization of Grayscale Image
![hist dip2](https://user-images.githubusercontent.com/94165415/230139161-686f17d2-6c8f-4fd8-804b-7311232cd1e4.png)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
