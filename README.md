# EDGEDETECTION

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary modules.
### Step2:
For performing edge detection on a image.
### Sobel
sobelx=cv2.Sobel(gray,cv2.CV_64F,1,0,5) 

sobely=cv2.Sobel(gray,cv2.CV_64F,0,1,5) 

sobelxy=cv2.Sobel(gray,cv2.CV_64F,1,1,5)
### Laplacian
lap=cv2.Laplacian(gray,cv2.CV_64F)
### Canny
canny=cv2.Canny(gray,120,150)
### Step3:
Display all the images with their respective edge detected images.
## Program:
```
Developed by: M.CHANDRU
Register no : 212222230026
```
# Import the packages
```python
import cv2
import matplotlib.pyplot as plt
```
# Load the image, Convert to grayscale and remove noise
```python
img=cv2.imread("moon.jpeg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
# SOBEL EDGE DETECTOR
### SOBEL X AXIS :
```python
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
### SOBEL Y AXIS :
```python
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
### SOBEL XY AXIS :
```python
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
# LAPLACIAN EDGE DETECTOR
```python
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
# CANNY EDGE DETECTOR
```python
canny=cv2.Canny(gray,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:
### SOBEL EDGE DETECTOR
### SOBEL X AXIS 
![Screenshot from 2023-10-04 13-13-02](https://github.com/chandrumathiyazhagan/EDGEDETECTION/assets/119393023/743778d6-d352-445f-ae86-98730a557735)

### SOBEL Y AXIS 
![Screenshot from 2023-10-04 13-14-05](https://github.com/chandrumathiyazhagan/EDGEDETECTION/assets/119393023/19000d59-3047-44d2-b8eb-bbd0222e7b77)

### SOBEL XY AXIS
![Screenshot from 2023-10-04 13-27-38](https://github.com/chandrumathiyazhagan/EDGEDETECTION/assets/119393023/0098a08a-da9b-44ae-8372-05c7b223e8fd)

### LAPLACIAN EDGE DETECTOR
![Screenshot from 2023-10-04 13-27-42](https://github.com/chandrumathiyazhagan/EDGEDETECTION/assets/119393023/994d3ef8-4b6a-4fd3-a267-7dfc16d647ce)

### CANNY EDGE DETECTOR
![Screenshot from 2023-10-04 13-27-44](https://github.com/chandrumathiyazhagan/EDGEDETECTION/assets/119393023/5fe94ba3-0fa3-42e8-ac39-665d990ba2f9)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
