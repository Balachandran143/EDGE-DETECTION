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
```
 NAME: BALACHANDRAN S
 REG.NO:212222100008
 Convert image to grayscale and remove noise
```
```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("dog.jpeg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
## Sobel edge detection:
### Sobel x axis:

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
Sobel y axis:

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
###Sobel xy axis:

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

### LAPLACIAN EDGE DETECTOR:

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
### CANNY EDGE DETECTOR:

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
## SOBEL EDGE DETECTOR
### Sobel x axis:
![Screenshot 2024-05-08 000603](https://github.com/Balachandran143/EDGE-DETECTION/assets/118886489/4250ac26-5f9d-449f-951a-91b29cd1946f)

### Sobel y axis:
![Screenshot 2024-05-08 000616](https://github.com/Balachandran143/EDGE-DETECTION/assets/118886489/f4e52343-b0cf-4de6-8d03-34b4458d29c6)

### Sobel xy axis:
![Screenshot 2024-05-08 000628](https://github.com/Balachandran143/EDGE-DETECTION/assets/118886489/2f513894-7133-4eb8-adf6-eb1a82e7320e)

### LAPLACIAN EDGE DETECTOR
![Screenshot 2024-05-08 000636](https://github.com/Balachandran143/EDGE-DETECTION/assets/118886489/35676537-c3f6-4cd9-bc4e-0dad2b730a9b)

### CANNY EDGE DETECTOR
![Screenshot 2024-05-08 000644](https://github.com/Balachandran143/EDGE-DETECTION/assets/118886489/182cbe6d-46d7-4b7b-952d-59c14d2bded2)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
