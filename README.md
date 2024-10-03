# EDGE-DETECTION
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

## Program:

### Developed by: Iswarya P
### Register no: 212223230082

```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
# Load the image
```
image = cv2.imread('colour.jpeg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
## Output:
![Screenshot 2024-10-03 112548](https://github.com/user-attachments/assets/187e9d6b-1100-40fd-8e2f-b4f5346ded8f)

### SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
## Output:
![Screenshot 2024-10-03 112542](https://github.com/user-attachments/assets/e3f96b99-a317-4010-85c7-7caa634374fb)


### LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
## Output:
![Screenshot 2024-10-03 112535](https://github.com/user-attachments/assets/c7c012d9-e0e1-4f18-8b1b-dd575ce74bef)

### CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
```
## Output:
![Screenshot 2024-10-03 112523](https://github.com/user-attachments/assets/56be796d-88c0-4a12-826b-e17255d90bcf)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
