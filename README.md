![out19](https://github.com/AbishekAnand15/COLOR_CONVERSIONS_OF-IMAGE/assets/118706942/ac167d1b-c7cc-48c1-9b61-8581b10bd0bd)# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1: Choose an image and save it as a filename.jpg ,
### Step2: Use imread(filename, flags) to read the file.
### Step3: Use imshow(window_name, image) to display the image.
### Step4: Use imwrite(filename, image) to write the image.
### Step5: End the program and close the output image windows.
### Step6: Convert BGR and RGB to HSV and GRAY
### Step7: Convert HSV to RGB and BGR
### Step8: Convert RGB and BGR to YCrCb
### Step9: Split and Merge RGB Image
### Step10: Split and merge HSV Image

##### Program:
```
### Developed By: Abishek Xavier A
### Register Number: 212222230004
```
<table>
  <tr>
    <td width=50%>

### i) Read and display the image
```Python
    import cv2
    image=cv2.imread('space1.jpg',1)
    image=cv2.resize(image,(400,300))
    cv2.imshow('Abishek Xavier A',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
``` 
  </td>
  <td>

### OUTPUT:

 ![out 1](https://github.com/AbishekAnand15/COLOR_CONVERSIONS_OF-IMAGE/assets/118706942/18d66b3c-b3af-43b7-86cb-a87927234b5f)


  </td>
  </tr>

   <tr>
    <td width=50%>

### ii)Write the image
```Python
    import cv2
    image=cv2.imread('space1.jpg',0)
    cv2.imwrite('d.jpg',image)
```
  </td>
  <td>

### OUTPUT:

![Screenshot 2024-02-14 200035](https://github.com/AbishekAnand15/COLOR_CONVERSIONS_OF-IMAGE/assets/118706942/45ae6aa1-75de-489f-b9f6-5f5eb3422e15)

  </td>
  </tr>
  <tr>
    <td width=50%>

### iii)Shape of the Image
```Python
    import cv2
    image=cv2.imread('space1.jpg',1)
    print(image.shape)
```
  </td>
  <td>

### OUTPUT:
![Screenshot 2024-02-14 200045](https://github.com/AbishekAnand15/COLOR_CONVERSIONS_OF-IMAGE/assets/118706942/69d13d4b-18aa-42db-8ea6-29b110ddfd59)

  </td>
  </tr>
  <tr>
    <td>
      
### iv)Access rows and columns
```Python
    import random
    import cv2
    image=cv2.imread('space1.jpg',1)
    image=cv2.resize(image,(400,400))
    for i in range (150,200):
      for j in range(image.shape[1]):
          image[i][j]=[random.randint(0,255),
                       random.randint(0,255),
                       random.randint(0,255)] 
    cv2.imshow('part image',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
  </td>
  <td width="50%">

### OUTPUT:

 ![out2](https://github.com/AbishekAnand15/COLOR_CONVERSIONS_OF-IMAGE/assets/118706942/c73c2cf6-65a1-41b9-94af-ef871e0a942f)

  </td>
  </tr>
  <tr>
    <td width=50%>
      
### v)Cut and paste portion of image

 ```Python
    import cv2
    image=cv2.imread('space1.jpg',1)
    image=cv2.resize(image,(400,400))
    tag =image[130:200,110:190]
    image[110:180,120:200] = tag
    cv2.imshow('partimage1',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
  </td>
  <td>
    
### OUTPUT:

![out3](https://github.com/AbishekAnand15/COLOR_CONVERSIONS_OF-IMAGE/assets/118706942/541f079a-1dc0-4b1b-8623-53a4befe6eb5)

  </td>
  </tr>
</table>

### vi) BGR and RGB to HSV and GRAY
```Python
import cv2
img = cv2.imread('space1.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv1)
hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)
gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray1)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![out 4](https://github.com/AbishekAnand15/COLOR_CONVERSIONS_OF-IMAGE/assets/118706942/c8d95e50-c998-4dc7-9414-61e771d3e370)
![out5](https://github.com/AbishekAnand15/COLOR_CONVERSIONS_OF-IMAGE/assets/118706942/8754a33a-a06e-4709-9fca-d008c3eb3574)
![out6](https://github.com/AbishekAnand15/COLOR_CONVERSIONS_OF-IMAGE/assets/118706942/491eb665-cdc7-4902-b171-0a7730ddf5be)
![out7](https://github.com/AbishekAnand15/COLOR_CONVERSIONS_OF-IMAGE/assets/118706942/12240fde-4d5f-45c1-83a2-d2e40546b553)
![out8](https://github.com/AbishekAnand15/COLOR_CONVERSIONS_OF-IMAGE/assets/118706942/1106514c-0470-418a-88ad-cb1c288c1b77)


### vii) HSV to RGB and BGR
```Python
import cv2
img = cv2.imread('space1.jpg')
img = cv2.resize(img,(300,200))
img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)
RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![out9](https://github.com/AbishekAnand15/COLOR_CONVERSIONS_OF-IMAGE/assets/118706942/9eac2c3d-6d2a-49b3-8756-dcfc3668d210)
![out10](https://github.com/AbishekAnand15/COLOR_CONVERSIONS_OF-IMAGE/assets/118706942/f9e0adf7-6ea7-4757-8c26-7e160937778f)
![out11](https://github.com/AbishekAnand15/COLOR_CONVERSIONS_OF-IMAGE/assets/118706942/9fba2366-b094-4627-bef4-73a1c7ca1aa0)


### viii) RGB and BGR to YCrCb
```Python
import cv2
img = cv2.imread('space1.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![out12](https://github.com/AbishekAnand15/COLOR_CONVERSIONS_OF-IMAGE/assets/118706942/a45b81dd-17bc-4643-897f-b25c9d03deaa)
![out13](https://github.com/AbishekAnand15/COLOR_CONVERSIONS_OF-IMAGE/assets/118706942/5393a075-6457-412d-b017-b3285391f901)
![out14](https://github.com/AbishekAnand15/COLOR_CONVERSIONS_OF-IMAGE/assets/118706942/58269f8c-fc8b-44ef-872a-7a2cbe71a5fd)




### ix) Split and merge RGB Image
```Python
import cv2
img = cv2.imread('space1.jpg',1)
img = cv2.resize(img,(300,200))
R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]
cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)
merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![out15](https://github.com/AbishekAnand15/COLOR_CONVERSIONS_OF-IMAGE/assets/118706942/9a1f7154-720e-4efc-9359-f4d8c1d28a7c)
![out16](https://github.com/AbishekAnand15/COLOR_CONVERSIONS_OF-IMAGE/assets/118706942/1a172b0e-1a47-471b-bb85-ccb3bdeae535)
![out17](https://github.com/AbishekAnand15/COLOR_CONVERSIONS_OF-IMAGE/assets/118706942/c5babc58-6f0c-4dc2-a360-7c2d1065f946)
![out18](https://github.com/AbishekAnand15/COLOR_CONVERSIONS_OF-IMAGE/assets/118706942/72658dd2-67d7-44b8-831a-efa1a5adbb21)



### x) Split and merge HSV Image
```Python
import cv2
img = cv2.imread("space1.jpg",1)
img = cv2.resize(img,(300,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
H,S,V=cv2.split(img)
cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)
merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![out19](https://github.com/AbishekAnand15/COLOR_CONVERSIONS_OF-IMAGE/assets/118706942/10928bf3-eaab-48ca-b8e9-3ba8656d0685)
![out20](https://github.com/AbishekAnand15/COLOR_CONVERSIONS_OF-IMAGE/assets/118706942/84d8468d-69d6-42f5-a8aa-27321e2c9934)
![out21](https://github.com/AbishekAnand15/COLOR_CONVERSIONS_OF-IMAGE/assets/118706942/87dce6e0-9757-475c-9764-c2c64eea3407)
![out22](https://github.com/AbishekAnand15/COLOR_CONVERSIONS_OF-IMAGE/assets/118706942/22265ae5-cadb-4230-95b2-ecdc3e3a7580)


## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







