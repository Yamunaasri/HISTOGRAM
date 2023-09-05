# HISTOGRAM
# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import cv2 and matplotlib.pyplot
<br>

### Step2:
Read and display the input images
<br>

### Step3:
Calculate the Histogram Values using calcHist()
<br>

### Step4:
Display the histograms
<br>

### Step5:
Calculate and display the equalized image using equalizeHist()
<br>

## Program:
```
# Developed By: T S Yamunaasri
# Register Number: 212222240117
import cv2
import matplotlib.pyplot as plt

# Histogram for Gray scale and Color image
 
gray_image = cv2.imread('grayscale.jpeg')
color_image = cv2.imread('color.jpeg')
plt.imshow(gray_image)
plt.show()
plt.imshow(color_image)
plt.show()
hist = cv2.calcHist([gray_image],[0],None,[256],[0,256])
hist1 = cv2.calcHist([color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('GrayScaleValue')
plt.ylabel('PixelCount')
plt.stem(hist)
plt.show()
plt.figure()
plt.title("Histogram")
plt.xlabel('Intensity Value')
plt.ylabel('PixelCount')
plt.stem(hist1)
plt.show()



# Equalized Image
import cv2
Gray_image=cv2.imread('gray.jpeg',0)
equ = cv2.equalizeHist(Gray_image)
cv2.imshow('Gray Image',Gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:
### Input Grayscale Image and Color Image
Gray Scale Image
![Screenshot 2023-09-05 144000](https://github.com/Yamunaasri/HISTOGRAM/assets/115707860/cac839c1-327c-4b1a-b33c-f3add928875b)

Color Image
![Screenshot 2023-09-05 144007](https://github.com/Yamunaasri/HISTOGRAM/assets/115707860/db87967b-2b07-4bdc-be6c-bd7daf961482)

<br>

### Histogram of Grayscale Image and any channel of Color Image
Gray Scale Image
![Screenshot 2023-09-05 144016](https://github.com/Yamunaasri/HISTOGRAM/assets/115707860/f8f5a8f8-2fbc-4864-80a9-4e9bb6cff752)

Color Image
![Screenshot 2023-09-05 144023](https://github.com/Yamunaasri/HISTOGRAM/assets/115707860/55bce756-c55e-4ef8-bcbb-184c38ff99fe)

<br>

### Histogram Equalization of Grayscale Image
Original Image
![Screenshot 2023-09-05 144411](https://github.com/Yamunaasri/HISTOGRAM/assets/115707860/a9292599-3dd0-4387-bcdc-3b73e7901601)

Equalized Image
![Screenshot 2023-09-05 144420](https://github.com/Yamunaasri/HISTOGRAM/assets/115707860/0ee182cd-5729-41b5-b88d-81fe1f7a9754)

<br>

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
