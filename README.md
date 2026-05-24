# Exp-10--Record-IMPLEMENTATION-OF-OPENING-AND-CLOSING
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

Create the Text using cv2.putText

### Step3:

Create the structuring element

### Step4:

Use Opening operation

### Step5:

Use Closing Operation

 
## Program:

``` Python


import cv2
import numpy as np
import matplotlib.pyplot as plt
img = np.zeros((100, 550), dtype = 'uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, 'Ayisha Rinsi K', (5,70), font, 2, (255), 5, cv2.LINE_AA)
n_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(n_img)
plt.axis("off")
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (11,11)
image_open = cv2.morphologyEx(n_img, cv2.MORPH_OPEN, kernel)
plt.imshow(image_open)
plt.axis("off")

image_close = cv2.morphologyEx(n_img, cv2.MORPH_CLOSE, kernel)
plt.imshow(image_close)
plt.axis("off")






```
## Output:

### Display the input Image

<img width="422" height="748" alt="image" src="https://github.com/user-attachments/assets/0a31ae24-722a-48b2-b43e-027cce257274" />

### Display the result of Opening

<img width="483" height="515" alt="image" src="https://github.com/user-attachments/assets/eaa516c0-5575-47f9-a764-2cbfb1e89f8a" />


### Display the result of Closing

<img width="485" height="512" alt="image" src="https://github.com/user-attachments/assets/3efdcfe9-ab6f-4edb-a0b2-1eb4ef0709d0" />

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
