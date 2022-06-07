# Implementation-of-Erosion-and-Dilation

## Aim
To implement Erosion and Dilation using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the Text using cv2.putText.

### Step3:
Create the structuring element.

### Step4:
Erode the image using cv2.erode().

### Step5:
Dilate the image using cv2.dilate().

 
## Program:

```python

# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt
# Load the Image
img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL
# Create the Text using cv2.putText
cv2.putText(img1,'VENKATESH',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img1,cmap='gray')
# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
# Erode the image
img_erode=cv2.erode(img1,kernel1)
plt.imshow(img_erode,cmap='gray')

# Dilate the image
img_dilate=cv2.dilate(img1,kernel1)
plt.imshow(img_dilate,cmap='gray')


```
## Output:

### Display the input Image



![v1](https://user-images.githubusercontent.com/75234983/172303373-b93ace68-faa5-4ea9-a9e3-71b24d3dc3fa.png)



### Display the Eroded Image




![v2](https://user-images.githubusercontent.com/75234983/172303398-606250ad-3e4f-4f0b-8368-39f783b3c51f.png)


### Display the Dilated Image


![v3](https://user-images.githubusercontent.com/75234983/172303421-377c1ce7-4da6-46b3-beed-894ac15296db.png)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
