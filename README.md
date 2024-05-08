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
Developed By:Varsha G

Register Number: 212222230166
## Input Grayscale Image and Color Image :
```
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("grayretriever.jpg")
color_image = cv2.imread("colorretriever.jpg")
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Color Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Histogram of Grayscale Image and any channel of Color Image :
```
import numpy as np
import cv2
Gray_image = cv2.imread("grayretriever.jpg")
Color_image = cv2.imread("colorretriever.jpg")
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
## Histogram Equalization of Grayscale Image :
```
import cv2
gray_image = cv2.imread("grayretriever.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/janani225/Histogram-of-an-images/assets/113497333/2033f7e1-9efc-4781-9365-bbd15c60df8e)


### Histogram of Grayscale Image and any channel of Color Image
![image](https://github.com/janani225/Histogram-of-an-images/assets/113497333/e71f96d4-4362-48e1-bc1a-d98fc49ad0b4)
![image](https://github.com/janani225/Histogram-of-an-images/assets/113497333/6e2c0158-651f-4b2a-8434-075d2d93eff2)
![image](https://github.com/janani225/Histogram-of-an-images/assets/113497333/63198d54-4290-4453-ac50-02eadd7d4f05)
![image](https://github.com/janani225/Histogram-of-an-images/assets/113497333/b7cd69d1-c963-46f3-a062-6ac07ed84779)



### Histogram Equalization of Grayscale Image.
![image](https://github.com/janani225/Histogram-of-an-images/assets/113497333/8f9a3340-8c48-49d7-a37b-456dab8d8acd)




## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
