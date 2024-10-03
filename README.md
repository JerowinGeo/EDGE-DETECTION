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

## Code:
```
import cv2
# Read the image
image = cv2.imread('username.jpg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

# Apply Gaussian blur
img_blurred = cv2.GaussianBlur(gray_image, (3, 3), 0)

# Sobel edge detection
sobelx = cv2.Sobel(img_blurred, cv2.CV_64F, 1, 0, ksize=5)
sobely = cv2.Sobel(img_blurred, cv2.CV_64F, 0, 1, ksize=5)
sobelxy = cv2.Sobel(img_blurred, cv2.CV_64F, 1, 1, ksize=5)

# Laplacian edge detection
laplacian = cv2.Laplacian(img_blurred, cv2.CV_64F)

# Canny edge detection
canny_edges = cv2.Canny(img_blurred, 120, 150)

# Display images
cv2.imshow('Original', gray_image)
cv2.imshow('Sobel X', sobelx)
cv2.imshow('Sobel Y', sobely)
cv2.imshow('Sobel XY', sobelxy)
cv2.imshow('Laplacian', laplacian)
cv2.imshow('Canny Edges', canny_edges)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:

### SOBEL EDGE DETECTOR

![image](https://github.com/user-attachments/assets/843bc85e-ca97-4e0a-91b6-9969d1eca559)

![image](https://github.com/user-attachments/assets/9ab64f0a-602d-4c83-8c45-f5a0a41863b2)

![image](https://github.com/user-attachments/assets/37eab91f-43ef-43e0-823d-16ab2273f280)




### LAPLACIAN EDGE DETECTOR
![image](https://github.com/user-attachments/assets/7405f393-122f-4799-8fe8-8884c9ac9b5a)



### CANNY EDGE DETECTOR
![image](https://github.com/user-attachments/assets/5e6756c9-de01-437b-b2cc-90dc25b3a049)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
