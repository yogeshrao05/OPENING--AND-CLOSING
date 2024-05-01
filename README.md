# EX 10 OPENING AND CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
- Step1: Import the necessary packages
- Step2: Give the input text using cv2.putText()
- Step3: Perform opening operation and display the result
- Step4: Similarly, perform closing operation and display the result
## Program:
```
NAME: YOGESH RAO S D
REG.No:212222110055
``` 
# Import the necessary packages
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
```python
img1=np.zeros((100,400), dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'Datascientist',(5,70), font,2,(255),5,cv2.LINE_AA)
```
# Create the structuring element
```python
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
# Use Opening operation
```python
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel)
plt.imshow(image1)
plt.axis("off")
```
# Use Closing Operation
```python
image2=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2)
plt.axis("off")
```
## Output:
### Display the input Image
![1daa](https://github.com/deepikasrinivasans/OPENING--AND-CLOSING/assets/119393935/b4990b49-f6c8-402f-8d9e-5beeb1f11e01)
### Display the result of Opening
![2daa](https://github.com/deepikasrinivasans/OPENING--AND-CLOSING/assets/119393935/b42639d0-7cc0-44cf-a300-2cd69ca337ef)
### Display the result of Closing
![3daa](https://github.com/deepikasrinivasans/OPENING--AND-CLOSING/assets/119393935/c96dd44c-b85a-4253-8607-7555fbb21c25)
## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
