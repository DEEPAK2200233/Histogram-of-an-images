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

### Developed By: DEEPAK RAJ S
### Register Number: 212222240023

### Colour and Gray Image:
```
import cv2
from matplotlib import pyplot as plt
# Load the color image
image = cv2.imread('Spb.jpeg')
# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
```
```
# Load the color image
image = cv2.imread('SPB Dark.jpg')
# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
```
### Histogram of Grayscale Image:
```
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])

```

### Histogram Equalization of Grayscale Image:
```
# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])
```
## Output:

### Input Image
![kamal3](https://github.com/user-attachments/assets/96d80c36-af17-4169-a757-6b751160dadf)

![kamal1](https://github.com/user-attachments/assets/c8a8a9d2-8e7c-497a-b1f4-a5c790a0bdd8)

### Histogram of Grayscale Image
![image](https://github.com/user-attachments/assets/b0552179-d6f9-4a37-aad2-fa83c482d9e0)  ![image](https://github.com/user-attachments/assets/655e94fe-e223-4aad-a649-9dc2e0db9dca)


![image](https://github.com/user-attachments/assets/9459c731-f1e5-4034-87f0-4b15e5cd4c80) ![image](https://github.com/user-attachments/assets/b288a5c2-a87a-4e03-ac98-1bb054e111af)


### Histogram Equalization of Grayscale Image.
![image](https://github.com/user-attachments/assets/e5ef5cac-a13e-4ce0-9afb-0374318c22b6)
![image](https://github.com/user-attachments/assets/bdf7c032-0c16-41af-9814-7c25a0d78865)

![image](https://github.com/user-attachments/assets/b3fd6a5a-e811-43b2-89e9-535db9b5e990)
![image](https://github.com/user-attachments/assets/b28c09fc-af42-446a-a673-a597748c1c6c)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
