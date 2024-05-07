# Exp:09 Implementation of Erosion and Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary pacakages
### Step2:
Create the text using cv2.putText
### Step3:
Create the structuring element
### Step4:
Erode the image
### Step5:
Dilate the Image
## Program:
DEVELOPED BY : SABARI AKASH A

REGISTER NO: 212222230124
``` Python
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'HEALTH',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')

# Create the structuring element
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)

# Erode the image
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')

# Dilate the image
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```
## Output:
### Display the input Image
![download](https://github.com/Sabariakash22009103/erosion--dilation/assets/119390227/e0d79dd9-0a51-421a-aa52-cc2fc9bd4120)
# structuring element
![image](https://github.com/Sabariakash22009103/erosion--dilation/assets/119390227/d90ab879-a93c-4a37-b50b-9acb320d84ed)
### Display the Eroded Image
![download](https://github.com/Sabariakash22009103/erosion--dilation/assets/119390227/9983fe29-30ea-480a-baea-02c9a1451d73)
### Display the Dilated Image
![download](https://github.com/Sabariakash22009103/erosion--dilation/assets/119390227/2998a37f-9c24-4ccb-a334-d894fe33ec2c)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
