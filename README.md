# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages

### Step2:
Give the input text using cv2.putText()

### Step3:
Perform opening operation and display the result

### Step4:
Similarly, perform closing operation and display the result

## Program:
### NAME : MUHAMMED AIMAN S
### REG NO : 212224240097
``` Python
# Import necessary packages
import cv2
import numpy as np
from matplotlib import pyplot as plt
from google.colab.patches import cv2_imshow

# i) Create the text using cv2.putText
img1 = np.zeros((300, 600), dtype='uint8')
font = cv2.FONT_ITALIC
img2 = cv2.putText(img1, "MUHAMMED AIMAN S", (5, 200), font, 2, (255), 6, cv2.LINE_AA)

cv2_imshow(img2)

# ii) Create structuring elements
kernel1 = cv2.getStructuringElement(cv2.MORPH_RECT, (11, 11))
kernel2 = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))

# iii) Use Opening operation (Erosion followed by Dilation)
img_open = cv2.morphologyEx(img2, cv2.MORPH_OPEN, kernel2)
cv2_imshow(img_open)

# iv) Use Closing operation (Dilation followed by Erosion)
img_close = cv2.morphologyEx(img2, cv2.MORPH_CLOSE, kernel1)
cv2_imshow(img_close)



```
## Output:

### Display the input Image
<br>
<img width="782" height="381" alt="image" src="https://github.com/user-attachments/assets/ec5cce07-4de2-4306-ab1b-e8d03378048b" />


<br>
<br>
<br>
<br>
<br>

### Display the result of Opening
<br>
<img width="757" height="377" alt="image" src="https://github.com/user-attachments/assets/b911b28e-7fb0-44f5-945b-e96f6c36a62a" />


<br>
<br>
<br>
<br>
<br>

### Display the result of Closing
<br>
<img width="757" height="367" alt="image" src="https://github.com/user-attachments/assets/5ec29ca6-a65f-46c3-b836-0ae9adef353a" />


<br>
<br>
<br>
<br>
<br>

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
