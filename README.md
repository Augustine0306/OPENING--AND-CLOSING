## OPENING--AND-CLOSING
### Aim
To implement Opening and Closing using Python and OpenCV.

### Software Required
1. Anaconda - Python 3.7
2. OpenCV
### Algorithm:
#### Step1:
Import the necessary packages
#### Step2:
Create the Text using cv2.putText
#### Step3:
Create the structuring element
#### Step4:
Use Opening operation
#### Step5:
Use Closing Operation

 
### Program:
```
Developed by: AUGUSTINE J
Register Number:212222240015
```
#### Display the input Image
```
import cv2
import numpy as np

img = np.zeros((350, 1400), dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img, 'ICE AGE', (15, 200), font, 5, (255), 10, cv2.LINE_AA)
cv2.imshow('created_text', img)
cv2.waitKey(0)
```
#### Create ths structured element
```
struct_ele = np.ones((9, 9), np.uint8)
```
#### Display the result of Opening
```
opening = cv2.morphologyEx(img, cv2.MORPH_OPEN, struct_ele)
cv2.imshow('Opening', opening)
cv2.waitKey(0)
```
#### Display the result of Closing
```
closing = cv2.morphologyEx(img, cv2.MORPH_CLOSE, struct_ele)
cv2.imshow('Closing', closing)
cv2.waitKey(0)
```
## Output:

### Display the input Image
![image](https://github.com/Augustine0306/OPENING--AND-CLOSING/assets/119404460/b74b57f4-abe3-4d71-98c8-2c8583a8770a)


### Display the result of Opening
![image](https://github.com/Augustine0306/OPENING--AND-CLOSING/assets/119404460/7928c24c-c507-43f7-bc75-63174e4031f3)

### Display the result of Closing
![image](https://github.com/Augustine0306/OPENING--AND-CLOSING/assets/119404460/85df0733-8b46-4a57-b7ed-5c7fc8096a02)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
