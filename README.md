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

### Developed By: Sriram G
### Register Number: 212222230149

```
import cv2
image = cv2.imread('kamal1.jpg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
cv2.imwrite('kamal2.jpg', gray_image)
cv2.imshow('Grayscale Image', gray_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
import numpy as np
import cv2
Gray_image = cv2.imread("kamal2.jpg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
import cv2
gray_image = cv2.imread("kamal2.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.imwrite("Black.jpg",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
import numpy as np
import cv2
import matplotlib.pyplot as plt
Gray_image = cv2.imread("Grey.jpg", cv2.IMREAD_GRAYSCALE)
EQU_image = cv2.imread("Black.jpg", cv2.IMREAD_GRAYSCALE)
gray_hist = cv2.calcHist([Gray_image], [0], None, [256], [0, 256])
equ_hist = cv2.calcHist([EQU_image], [0], None, [256], [0, 256])
gray_hist = cv2.normalize(gray_hist, gray_hist).flatten()
equ_hist = cv2.normalize(equ_hist, equ_hist).flatten()
plt.figure()
plt.title("Histogram Comparison")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.plot(gray_hist, color='blue', label='Gray Image Histogram')
plt.plot(equ_hist, color='red', label='EQU Image Histogram')
plt.legend()
plt.show()
```
## Output:

### Input Image
![image](https://github.com/user-attachments/assets/9f28b787-02bb-4768-a5df-d679f92988ea)


### Histogram of Grayscale Image
![image](https://github.com/user-attachments/assets/68d932a5-0045-4b53-91fd-686681c6b471)
![image](https://github.com/user-attachments/assets/1946ff2a-610d-43aa-bf1f-6abea5ada1cf)

### Histogram Equalization of Grayscale Image.
![image](https://github.com/user-attachments/assets/ad397612-ab58-4f71-8bfc-b4cf6f7d92d1)

![image](https://github.com/user-attachments/assets/d4406218-0287-4645-ad87-407477e6c192)





## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
