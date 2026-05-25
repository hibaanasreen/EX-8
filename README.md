# THRESHOLDING

## AIM:
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## SOFTWARE REQUIRED:
1. Anaconda - Python 3.7
2. OpenCV

## ALGORITHM:

### Step1:
Load the necessary packages.

### Step2:
Read the Image and convert to grayscale.

### Step3:
Use Global thresholding to segment the image.

### Step4:
Use Adaptive thresholding to segment the image.

### Step5:
Use Otsu's method to segment the image and display the results.

## PROGRAM:
```
DEVELOPED BY : HIBA NASREEN M
REG NO : 212224040117
```
```
# Load the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
```

# Read the Image and convert to grayscale
image = cv2.imread('my image.jpg')  # Replace with your image file path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)  # Convert to grayscale
plt.subplot(1, 1, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert from BGR to RGB for display
plt.title("Original Image")
plt.axis('off')
```
```

# Use Global thresholding to segment the image
_, global_thresholded = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)
```
```

# Use Adaptive thresholding to segment the image
adaptive_thresholded = cv2.adaptiveThreshold(gray_image, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 11, 2)

```
```
# Use Otsu's method to segment the image 
_, otsu_thresholded = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)

```
```
# Display the results
# Global Thresholding
plt.subplot(2, 2, 2)
plt.imshow(global_thresholded, cmap='gray')
plt.title("Global Thresholding")
plt.axis('off')
```
```
# Adaptive Thresholding
plt.subplot(2, 2, 3)
plt.imshow(adaptive_thresholded, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis('off')
```
```
# Otsu's Method
plt.subplot(2, 2, 4)
plt.imshow(otsu_thresholded, cmap='gray')
plt.title("Otsu's Method")
plt.axis('off')
```
```
# Show the plot
plt.tight_layout()
plt.show()
```
## Output :

### Original Image
<img width="280" height="509" alt="image" src="https://github.com/user-attachments/assets/080b2dd7-938d-4bf4-968a-e591647fc90d" />


### Global Thresholding
 
<img width="281" height="502" alt="image" src="https://github.com/user-attachments/assets/7f86aa10-fc1a-49b4-9bcc-f09e94afb22b" />


### Adaptive Thresholding
 
<img width="283" height="501" alt="image" src="https://github.com/user-attachments/assets/871980c7-32ae-4c41-a5eb-14ee6e3417c7" />


### Optimum Global Thesholding using Otsu's Method
 
<img width="277" height="507" alt="image" src="https://github.com/user-attachments/assets/671756d7-0591-4c58-9792-1ff2d2c249e2" />


## RESULT:
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
