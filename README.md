# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
   Read an image using imread() and Convert BGR and RGB to HSV and GRAY<br>
  using:<br>
  cv2.cvtColor(image,cv2.COLOR_RGB2HSV)<br>
  cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)<br>
  cv2.cvtColor(image,cv2.COLOR_BGR2HSV)<br>
  cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
  
### Step2:
  Convert HSV to RGB and BGR<br>
  using:<br>
  cv2.cvtColor(image,cv2.COLOR_HSV2RGB)<br>
  cv2.cvtColor(image,cv2.COLOR_HSV2BGR)  
### Step3:
  Convert RGB and BGR to YCrCb<br>
    using:<br>
    cv2.cvtColor(image,cv2.COLOR_RGB2YCrCb)<br>
    cv2.cvtColor(image,cv2.COLOR_BGR2YCrCb)
### Step4:
   Split and Merge RGB Image<br>
    using:<br>
    blue = image[:,:,0]<br>
    green = image[:,:,1]<br>
    red = image[:,:,2]<br>
    cv2.merge((blue,green,red))

### Step5:
   Split and merge HSV Image<br>
    using:<br>
    hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)<br>
    h, s, v = cv2.split(hsv)<br>
    cv2.merge((h,s,v))

## Program:
```python
# Developed By: R ARUNRAJ
# Register Number: 212220230004
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
<img src="https://user-images.githubusercontent.com/75235747/162788699-9cd90b37-940f-422d-a249-6a7bf736f84e.png" width="700">
<img src="https://user-images.githubusercontent.com/75235747/162788847-b1e4cddb-084d-4875-a7d2-a4ed160b097b.png" width="700">

### ii) HSV to RGB and BGR
<img src="https://user-images.githubusercontent.com/75235747/162789029-7e0a73ce-a660-4254-be53-5aae19471b87.png" width="700">

### iii) RGB and BGR to YCrCb
<img src="https://user-images.githubusercontent.com/75235747/162789231-243ca0d5-46a0-4076-8d9b-ce2ff34ee8da.png" width="700">

### iv) Split and merge RGB Image
<br>
<img src="https://user-images.githubusercontent.com/75235747/162789569-8c713137-bf89-44cc-b618-407084364536.png" width="700">
<img src="https://user-images.githubusercontent.com/75235747/162789771-388195c2-c6be-49f5-b5e2-3da1462af417.png" width="700">

### v) Split and merge HSV Image
<img src="https://user-images.githubusercontent.com/75235747/162789828-ff4cec00-ea01-441e-9ec2-dbdf374ed6f8.png" width="700">
<img src="https://user-images.githubusercontent.com/75235747/162789860-919d721c-e4cf-4622-b7d4-93f1609f3c97.png" width="700">
<img src="https://user-images.githubusercontent.com/75235747/162789892-67c98072-0148-4928-9c60-a78af665b15d.png" width="700">

## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
