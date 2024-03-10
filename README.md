# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().

### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```
# Developed By: 212222103002
# Register Number: V.Sriram
```
## Input Grayscale Image and Color Image :
```
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("image1.jpg")
color_image = cv2.imread("image2.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Histogram of Grayscale Image and any channel of Color Image:
```
import numpy as np
import cv2
Gray_image = cv2.imread("image1.jpg")
Color_image = cv2.imread("image2.jpg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
## Histogram Equalization of Grayscale Image:
```
import cv2
gray_image = cv2.imread("image1.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image
![Screenshot 2024-03-10 092652](https://github.com/Darkwebnew/Histogram-of-an-images/assets/143114486/4fd648e9-5cfa-447d-8272-3537e3fe09b9)
![Screenshot 2024-03-10 092717](https://github.com/Darkwebnew/Histogram-of-an-images/assets/143114486/f9e0a339-cee5-4efd-93bd-e998b1c4f9aa)
### Histogram of Grayscale Image and any channel of Color Image
![Screenshot 2024-03-10 092829](https://github.com/Darkwebnew/Histogram-of-an-images/assets/143114486/04f94b3e-5b0f-42f9-a218-550ebf42dfe3)
![Screenshot 2024-03-10 092839](https://github.com/Darkwebnew/Histogram-of-an-images/assets/143114486/09fe03af-4d6f-45ba-b2b0-54db3f712d94)
![Screenshot 2024-03-10 092848](https://github.com/Darkwebnew/Histogram-of-an-images/assets/143114486/9a9464ff-0038-4507-897a-4cf56fcb356d)
![Screenshot 2024-03-10 092859](https://github.com/Darkwebnew/Histogram-of-an-images/assets/143114486/cbf0216e-23b6-4f66-9bf7-4d799d351874)
### Histogram Equalization of Grayscale Image.
![Screenshot 2024-03-10 092959](https://github.com/Darkwebnew/Histogram-of-an-images/assets/143114486/023c64f9-a5d7-4976-bf14-5f2dbacc7c90)
![Screenshot 2024-03-10 093015](https://github.com/Darkwebnew/Histogram-of-an-images/assets/143114486/7858bb48-c8ab-4995-b325-cfe2dc9675a1)
## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
