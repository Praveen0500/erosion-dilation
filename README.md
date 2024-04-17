# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
- Step1: Import the necessary packages
- Step2: Insert the text using cv2.putText()
- Step3: The perform the erosion for given text and display the text using imshow()
- Step4: Next,perform dilation for inout text and display the result
## Program:
```
DEVELOPED BY: PRAVEEN S
REGISTER NUMBER: 212222240078
```
### Import the necessary packages
```python
import cv2
import numpy as np 
import matplotlib.pyplot as plt
```
### Create the Text using cv2.putText
```python
img1=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'PRAVEEN',(7,70),font,2,(255),6,cv2.LINE_AA)
```
### Create the structuring element
```python
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
### Erode the image
```python
image_erode1=cv2.erode(img1,kernel1)
plt.imshow(image_erode1)
plt.axis("off")
```
### Dilate the image
```python
image_dilate1=cv2.dilate(img1,kernel1)
plt.imshow(image_dilate1)
plt.axis("off")
```
## Output:
### Display the input Image
![image](https://github.com/Praveen0500/erosion-dilation/assets/120218611/c9b48a94-c387-4cbd-aa61-0da4fc61fd06)

### Display the Eroded Image
![image](https://github.com/Praveen0500/erosion-dilation/assets/120218611/822d18ca-a857-45e1-bbb8-f35b3afc6916)

### Display the Dilated Image
![image](https://github.com/Praveen0500/erosion-dilation/assets/120218611/ff4cb7b2-7068-4c31-8fb1-790bf7ad2540)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
