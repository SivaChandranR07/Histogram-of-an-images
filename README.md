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

# Developed By: Siva Chandran R
# Register Number: 212222240099
# Input Grayscale Image and Color Image:
```py
import cv2
import matplotlib.pyplot as plt
Gray_image = cv2.imread('/dip1.jpeg')
Color_image = cv2.imread('/dip2.jpeg')
plt.imshow(Gray_image)
plt.show()
plt.imshow(Color_image)
plt.show()
```
# Histogram of Grayscale Image and Green channel of Color Image:
```py
hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
hist1 = cv2.calcHist([Color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()
plt.figure()
plt.title("Histogram of Color Image Green Channel")
plt.xlabel('Intensity value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()
```
# Histogram Equalization of Grayscale Image:
```py
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
```





## Output:
### Input Grayscale Image and Color Image:

![Screenshot 2024-03-19 110759](https://github.com/SivaChandranR07/Histogram-of-an-images/assets/113497395/581bfadf-09eb-48ee-a8f4-0736e1727ec8)



### Histogram of Grayscale Image and any channel of Color Image
![Screenshot 2024-03-19 111043](https://github.com/SivaChandranR07/Histogram-of-an-images/assets/113497395/a7caf22b-71c0-4a53-ac3b-a111bfdfc246)




## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
