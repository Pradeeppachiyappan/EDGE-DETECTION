# EDGE-DETECTION->
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:
Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## PROGRAM:

```
DEVELOPED BY : Pradeepraj P
REG NO: 212222240073
```
### ORIGINAL IMAGE
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread('Thor.jpg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
### OUTPUT
![download](https://github.com/user-attachments/assets/d8744aec-eec8-47c4-a720-0f1f01a21776)

### SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
### OUTPUT 
![download](https://github.com/user-attachments/assets/e47a52cb-ca08-488f-b495-6048d45f52d4)

### LAPLACIAN EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)
plt.imshow(sobel_x, cmap='gray')
plt.title('LAPLACIAN EDGE DETECTOR')
plt.axis('off')
```
### OUTPUT
![download](https://github.com/user-attachments/assets/14a5b0f3-abb3-4521-bff7-433470e03806)

### CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
```
### OUTPUT
![download](https://github.com/user-attachments/assets/880f3866-1a9f-46d0-927d-2104a0682e43)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
