#exp 10
#  Record-IMPLEMENTATION OF OPENING AND CLOSING
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
Open the image

### Step5
close the Image
 
## Developed by: Angelin gracy.R
## Register number: 212225240009
## PROGRAM
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = np.zeros((500, 500, 3), dtype=np.uint8)


font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Open and Close', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)


```

<img width="518" height="828" alt="image" src="https://github.com/user-attachments/assets/848052d4-dc33-4355-b2a1-de39177ce43a" />


```
kernel = np.ones((3, 3), np.uint8)

plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')

````

<img width="389" height="410" alt="download" src="https://github.com/user-attachments/assets/6b0b4b35-1ab9-4503-a99c-8b0a93a0cccf" />


````

opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)

plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Opening Operation")
plt.axis('off')


````
<img width="389" height="410" alt="download" src="https://github.com/user-attachments/assets/11429cef-3cfc-4f95-bf7f-f2a7f7053fbc" />


````
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)


````










## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
