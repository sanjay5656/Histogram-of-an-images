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

### Developed By    : Sanjay S 
### Register Number : 212221243002
```python
import cv2
import matplotlib.pyplot as plt
Gray_image = cv2.imread('dip_ex03_grey.jpeg')
Color_image = cv2.imread('dip_ex03_color.jpg')
plt.imshow(Gray_image)
plt.show()
plt.imshow(Color_image)
plt.show()

hist=cv2.calcHist([Gray_image],[0],None,[256],[0,256])
hist1=cv2.calcHist([Color_image],[1],None,[256],[0,256])

plt.figure()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()

plt.figure()
plt.title("Histogram")
plt.xlabel('color value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()

gray_image=cv2.imread("dip_ex03_grey.jpeg",0)
equ=cv2.equalizeHist(gray_image)
cv2.imshow("Equlaized image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image
![grey](https://github.com/sanjay5656/Histogram-of-an-images/assets/115128955/e5e9d119-cf02-4ceb-a73d-dbd06012b438)
![color](https://github.com/sanjay5656/Histogram-of-an-images/assets/115128955/2e342273-fb7d-4a35-bf25-8bdca6d21498)

### Histogram of Grayscale Image and any channel of Color Image
### Gray image:
![Screenshot 2024-03-19 114339](https://github.com/sanjay5656/Histogram-of-an-images/assets/115128955/a98a9b60-278b-44ee-8b41-7c4e45d92bd9)

![Screenshot 2024-03-19 114535](https://github.com/sanjay5656/Histogram-of-an-images/assets/115128955/56981fde-0854-4bae-8fc1-3d204b473cb8)

### color image:
![Screenshot 2024-03-19 114346](https://github.com/sanjay5656/Histogram-of-an-images/assets/115128955/221b6c99-1c50-4d76-bdfa-f143b5e0513d)

![Screenshot 2024-03-19 114541](https://github.com/sanjay5656/Histogram-of-an-images/assets/115128955/27e95a02-266a-4f50-b21b-a69ccf1ae449)

### Histogram Equalization of Grayscale Image.
![grey](https://github.com/sanjay5656/Histogram-of-an-images/assets/115128955/39229e27-4995-443c-b1e8-49df475c2c70)
![Equlaized](https://github.com/sanjay5656/Histogram-of-an-images/assets/115128955/c9b05e5f-e794-4d55-ab5f-7097fb6313b5)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
