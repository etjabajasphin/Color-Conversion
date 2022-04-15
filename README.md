# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
```
Read an image using imread() and Convert BGR and RGB to HSV and GRAY
using:
cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
```
### Step2:
```
Convert HSV to RGB and BGR
using:
cv2.cvtColor(image,cv2.COLOR_HSV2RGB)
cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
```
### Step3:
```
Convert RGB and BGR to YCrCb
using:
cv2.cvtColor(image,cv2.COLOR_RGB2YCrCb)
cv2.cvtColor(image,cv2.COLOR_BGR2YCrCb)
```
### Step4:
```
Split and Merge RGB Image
using:
blue = image[:,:,0]
green = image[:,:,1]
red = image[:,:,2]
cv2.merge((blue,green,red))
```
### Step5:
```
Split and merge HSV Image
using:
hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
h, s, v = cv2.split(hsv)
cv2.merge((h,s,v))
```
## Program:
# Developed By: S.Sumyuktha Rani
# Register Number: 212220230050
# i) Convert BGR and RGB to HSV and GRAY
```
import cv2
image=cv2.imread("pic.jpeg")
cv2.imshow("212220230040",image)
BGR_HSV=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.imshow("BGR to HSV image",BGR_HSV)
BGR_GRAY=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
cv2.imshow("BGR to GRAY image",BGR_GRAY)
RGB_HSV=cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.imshow("RGB to HSV image",RGB_HSV)
RGB_GRAY=cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.imshow("RGB to GRAY image",RGB_GRAY)
cv2.imshow("Apple",image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# ii)Convert HSV to RGB and BGR
```
hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.imshow("HSV image",hsv)
HSV_RGB=cv2.cvtColor(image,cv2.COLOR_HSV2RGB)
cv2.imshow("HSV to RGB image",HSV_RGB)
HSV_BGR=cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
cv2.imshow("HSV to BGR image",HSV_BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# iii)Convert RGB and BGR to YCrCb
```
RGB_YCrCb=cv2.cvtColor(image,cv2.COLOR_RGB2YCrCb)
cv2.imshow("RGB to YCrCb image",RGB_YCrCb)
BGR_YCrCb=cv2.cvtColor(image,cv2.COLOR_BGR2YCrCb)
cv2.imshow("BGR to YCrCb image",BGR_YCrCb)
cv2.imshow("panda",image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# iv)Split and Merge RGB Image
```
blue = image[:,:,0]
cv2.imshow("Blue Split",blue)
green = image[:,:,1]
cv2.imshow("Green Split",green)
red = image[:,:,2]
cv2.imshow("Red Split",red)
merged=cv2.merge((blue,green,red))
cv2.imshow("Merged Image",merged)
cv2.imshow("orange",image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# v) Split and merge HSV Image
```
hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
h, s, v = cv2.split(hsv)
cv2.imshow('h_plane', h)
cv2.imshow('s_plane', s)
cv2.imshow('v_plane', v)
mergedhsv=cv2.merge((h,s,v))
cv2.imshow("HSV image",hsv)
cv2.imshow('Merged HSV',mergedhsv)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### i) BGR and RGB to HSV and GRAY

![1a](https://user-images.githubusercontent.com/75235818/163591571-0901ab34-6d76-4d6b-be3e-1b6a468ceda9.jpeg)
![1b](https://user-images.githubusercontent.com/75235818/163591639-7c191664-28e0-47d9-9673-6767cbfdef12.jpeg)
![1c](https://user-images.githubusercontent.com/75235818/163591748-66304c37-1cd0-4700-a357-725e3b2d0e5b.jpeg)

### ii) HSV to RGB and BGR

![2a](https://user-images.githubusercontent.com/75235818/163591842-493dc683-b515-4d4f-89c9-a1c25bcee1b0.jpeg)

### iii) RGB and BGR to YCrCb

![3a](https://user-images.githubusercontent.com/75235818/163591983-13917feb-818e-46a2-8c9f-05e156f0377c.jpeg)

### iv) Split and merge RGB Image

![4a](https://user-images.githubusercontent.com/75235818/163592109-a1e02da5-5e3d-4adc-abd4-ec472a8adf22.jpeg)
![4b](https://user-images.githubusercontent.com/75235818/163592171-fb90c0f2-b72d-47bf-b4d6-2d248adf577d.jpeg)

### v) Split and merge HSV Image

![5a](https://user-images.githubusercontent.com/75235818/163592231-c7a6fd9a-840a-4401-ad40-effaea34e81d.jpeg)
![5b](https://user-images.githubusercontent.com/75235818/163592324-301f36ba-6986-4464-93ec-77ba7e726e33.jpeg)

## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
