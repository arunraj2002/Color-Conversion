# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
<br>
  Read an image using imread() and Convert BGR and RGB to HSV and GRAY
  using:
  cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
  cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
  cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
  cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
### Step2:
<br>
 Convert HSV to RGB and BGR
  using:
  cv2.cvtColor(image,cv2.COLOR_HSV2RGB)
  cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
### Step3:
<br>
   Convert RGB and BGR to YCrCb
    using:
    cv2.cvtColor(image,cv2.COLOR_RGB2YCrCb)
    cv2.cvtColor(image,cv2.COLOR_BGR2YCrCb)
### Step4:
<br>
   Split and Merge RGB Image
    using:
    blue = image[:,:,0]
    green = image[:,:,1]
    red = image[:,:,2]
    cv2.merge((blue,green,red))

### Step5:
<br>
   Split and merge HSV Image
    using:
    hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
    h, s, v = cv2.split(hsv)
    cv2.merge((h,s,v))

## Program:
```python
# Developed By:
# Register Number:
# i) Convert BGR and RGB to HSV and GRAY

    import cv2
    color=cv2.imread('tower.jpg')
    hsv=cv2.cvtColor(color,cv2.COLOR_BGR2HSV)
    cv2.imshow('BGR_HSV',hsv)
    hsv2=cv2.cvtColor(color,cv2.COLOR_RGB2HSV)
    cv2.imshow('RGB_HSV',hsv2)
    hsv3=cv2.cvtColor(color,cv2.COLOR_BGR2GRAY)
    cv2.imshow('BGR_GRAY',hsv3)
    hsv4=cv2.cvtColor(color,cv2.COLOR_RGB2GRAY)
    cv2.imshow('RGB_GRAY',hsv4)
    cv2.waitKey(0)
    cv2.destroyAllWindows()

# ii)Convert HSV to RGB and BGR

    rgb=cv2.cvtColor(hsv2,cv2.COLOR_HSV2RGB)
    cv2.imshow('HSV_RGB',rgb)
    bgr=cv2.cvtColor(hsv2,cv2.COLOR_HSV2BGR
    cv2.imshow('HSV_BGR',bgr) 
    cv2.waitKey(0)
    cv2.destroyAllWindows()

# iii)Convert RGB and BGR to YCrCb

    ycrcb=cv2.cvtColor(color,cv2.COLOR_RGB2YCrCb)
    cv2.imshow('RGB_YCrCB',ycrcb)
    ycrcb1=cv2.cvtColor(color,cv2.COLOR_BGR2YCrCb)
    cv2.imshow('BGR_YCrCB',ycrcb1)
    cv2.waitKey(0)
    cv2.destroyAllWindows()

# iv)Split and Merge RGB Image

    blue=color[:,:,0]
    green=color[:,:,1]
    red=color[:,:,2]
    cv2.merge((blue,green,red))
    cv2.imshow("blue",blue)
    cv2.imshow("green",green)
    cv2.imshow("red",red)
    cv2.waitKey(0)
    cv2.destroyAllWindows()

# v) Split and merge HSV Image

  hsv5=cv2.cvtColor(color,cv2.COLOR_BGR2HSV)
  cv2.imshow("ORIGINAL HSV",hsv5)
  h , s, v = cv2.split(hsv5)
  cv2.imshow('h_plane',h)
  cv2.imshow('s_plane',s)
  cv2.imshow('v_plane',v)
  mergedhsv=cv2.merge((h,s,v))
  cv2.imshow('merged',mergedhsv)
  cv2.waitKey(0)

```
## Output:
### i) BGR and RGB to HSV and GRAY
<br>
<br>

### ii) HSV to RGB and BGR
<br>
<br>

### iii) RGB and BGR to YCrCb
<br>
<br>

### iv) Split and merge RGB Image
<br>
<br>

### v) Split and merge HSV Image
<br>
<br>


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
