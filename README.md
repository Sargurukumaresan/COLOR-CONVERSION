# COLOR-CONVERSION
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
import cv2 library and upload the image or capture an image.
### Step2:
Read the saved image using cv2.imread("filename.jpg").
### Step3:
Convert the image into the given color transformation using cv2.cvtColor(image, cv2.BGR2YCrCb) and similarly for other color formats.
### Step4:
Split and merge the image using cv2.split(hsv) and cv2.merge([h,s,v]).
### Step5:
Output the image using cv2.imshow("OUTPUT", image).
## Program:
```python
# Developed By:SARGURU K
# Register Number:212222230134
# i) Convert BGR and RGB to HSV and GRAY
```python
import cv2
houseImage = cv2.imread('dip.jpg')
cv2.imshow('212222230134_SARGURU',houseImage)
hsvImage = cv2.cvtColor(houseImage,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsvImage)
hsvImage1=cv2.cvtColor(houseImage,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsvImage1)
grayImage = cv2.cvtColor(houseImage,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',grayImage)
grayImage1 = cv2.cvtColor(houseImage,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',grayImage1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# ii)Convert HSV to RGB and BGR
```python
import cv2
houseHSVImage = cv2.imread('dip.jpg')
cv2.imshow('212222230134_SARGURU',houseHSVImage)
RGBImage = cv2.cvtColor(houseHSVImage,cv2.COLOR_HSV2RGB)
cv2.imshow('BGR2HSV',RGBImage)
BGRImage=cv2.cvtColor(houseHSVImage,cv2.COLOR_HSV2BGR)
cv2.imshow('RGB2HSV',BGRImage)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# iii)Convert RGB and BGR to YCrCb
```python
import cv2
houseImage = cv2.imread('dip.jpg')
cv2.imshow('212222230134_SARGURU',houseImage)
YCrCb_image = cv2.cvtColor(houseImage, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR2HSV',YCrCb_image)
YCrCb_image1 = cv2.cvtColor(houseImage, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB2HSV',YCrCb_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# iv)Split and Merge RGB Image
```python
import cv2
image = cv2.imread('dip.jpg')
blue = image[:,:,0]
green = image[:,:,1]
red = image[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
mergeBgr = cv2.merge((blue,green,red))
cv2.imshow('212222230134_SARGURU',mergeBgr)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# v) Split and merge HSV Image
```python
import cv2
image = cv2.imread('dip.jpg')
hsv = cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
h,s,v = cv2.split(hsv)
cv2.imshow('Hue - Image',h)
cv2.imshow('Saturation - Image',s)
cv2.imshow('Gray - Image',v)
mergedHSV = cv2.merge((h,s,v))
cv2.imshow('212222230134_SARGURU',mergedHSV)
cv2.waitKey(0)
cv2.destroyAllWindow()
```
## Output:
### i) BGR and RGB to HSV and GRAY
![A1](https://github.com/Sargurukumaresan/COLOR-CONVERSION/assets/119559840/db1b6d40-476d-47fa-8233-c1cebdf132fa)

### ii) HSV to RGB and BGR
![A2](https://github.com/Sargurukumaresan/COLOR-CONVERSION/assets/119559840/822f9de0-428f-4e8f-8995-e964380b43da)


### iii) RGB and BGR to YCrCb
![A3](https://github.com/Sargurukumaresan/COLOR-CONVERSION/assets/119559840/df6838cc-ef19-493e-b672-e412f6c6c13c)


### iv) Split and merge RGB Image
![A4](https://github.com/Sargurukumaresan/COLOR-CONVERSION/assets/119559840/c815c23f-f982-42fa-9257-f4a66780b2c9)


### v) Split and merge HSV Image
![A5](https://github.com/Sargurukumaresan/COLOR-CONVERSION/assets/119559840/75278c98-de1f-4350-a804-976d34900f6e)


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
