# OPENING--AND-CLOSING
# NAME : Kesav Deepak Sridharan
# REG NO : 212223230104

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

``` Python
#NAME : Kesav Deepak Sridharan
#REG NO : 212223230104
# Import necessary packages
import cv2
import numpy as np
from matplotlib import pyplot as plt
from google.colab.patches import cv2_imshow

# i) Create the text using cv2.putText
img1 = np.zeros((300, 600), dtype='uint8')
font = cv2.FONT_ITALIC
img2 = cv2.putText(img1, "Kesav Deepak Sridharan", (5, 200), font, 2, (255), 6, cv2.LINE_AA)

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
<img width="389" height="411" alt="image" src="https://github.com/user-attachments/assets/7f644a9a-d9bf-45b5-8368-7009e8e04b1b" />




### Display the result of Opening
<img width="389" height="411" alt="image" src="https://github.com/user-attachments/assets/74a5b44c-77e6-4989-bcb3-bf36d9f093c9" />



### Display the result of Closing
<img width="389" height="411" alt="image" src="https://github.com/user-attachments/assets/cb8cdf52-545f-433d-beba-bbf5489d7e48" />



## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
