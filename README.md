# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the text image using cv2.putText.

### Step3:
Then create the structuring element for opening and closing.

### Step4:
Apply erosion and dilation using cv2.MORPH_OPEN and cv2.MORPH_CLOSE.

### Step5:
Plot the images using plt.imshow.

 
## Program:
```
Developed by : Kumaravel V
Registeration Number:212220230027
```

``` Python
# Import the necessary packages

import cv2
import numpy as np
import matplotlib.pyplot as plt


# Create the Text using cv2.putText

text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image," Gowri",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image,'magma')
plt.axis('off')


# Create the structuring element

kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(9,9))



# Use Opening operation

image1=cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("Opening")
plt.imshow(image1,'magma')
plt.axis('off')

# Use Closing Operation

image2=cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("Closing")
plt.imshow(image2,'magma')
plt.axis('off')



```
## Output:

### Display the input Image
![Screenshot_686](https://user-images.githubusercontent.com/75235455/170063650-3f388ad7-a570-4cf7-a9bb-8fe60db31ddd.png)
<br>
<br>
<br>
<br>
<br>
<br>

### Display the result of Opening
![Screenshot_687](https://user-images.githubusercontent.com/75235455/170063705-79e2ec19-d7bb-453a-b5ed-7cd7e144fd93.png)
<br>
<br>
<br>
<br>
<br>
<br>

### Display the result of Closing
![Screenshot_688](https://user-images.githubusercontent.com/75235455/170063757-a2480ef0-9a38-4a44-910e-e952acfbce55.png)
<br>
<br>
<br>
<br>
<br>
<br>

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
