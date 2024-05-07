
# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate the Image

## Program:
```
NAME: Karthick P
REG NO: 212222100021
```
### Import the necessary packages
``` Python

import numpy as np
import cv2
import matplotlib.pyplot as plt
```

### Create the Text using cv2.putText
``` Python
img = np.zeros((100,400),dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img,'KRISHNA',(40,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```
### Create the structuring element
``` Python
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
```
### Erode the image
``` Python
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
```
### Dilate the image
``` Python
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```
## Output:

### Display the input Image
![WhatsApp Image 2024-05-07 at 6 07 52 PM (1)](https://github.com/karthickprabakaran/erosion--dilation/assets/166775653/5e76c80c-5d0d-4ec1-b825-a0ee46e47ada)


### Display the Eroded Image
![WhatsApp Image 2024-05-07 at 6 07 52 PM](https://github.com/karthickprabakaran/erosion--dilation/assets/166775653/05037c90-727e-440c-b4ad-f6e7f08b94d1)


### Display the Dilated Image
![WhatsApp Image 2024-05-07 at 6 07 53 PM](https://github.com/karthickprabakaran/erosion--dilation/assets/166775653/7e4b68b7-24ce-46ef-8877-5e3db0c11aeb)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
