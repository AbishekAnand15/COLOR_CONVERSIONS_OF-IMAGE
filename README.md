# COLOR_CONVERSIONS_OF-IMAGE
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

 <img src="![out 1](https://github.com/AbishekAnand15/COLOR_CONVERSIONS_OF-IMAGE/assets/118706942/6bd6d7aa-10d3-4ffc-89e9-f4c74187f7c4)
">
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

<img src="![Screenshot 2024-02-14 200035](https://github.com/AbishekAnand15/COLOR_CONVERSIONS_OF-IMAGE/assets/118706942/45ae6aa1-75de-489f-b9f6-5f5eb3422e15)
">
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
<img src="![Screenshot 2024-02-14 200045](https://github.com/AbishekAnand15/COLOR_CONVERSIONS_OF-IMAGE/assets/118706942/69d13d4b-18aa-42db-8ea6-29b110ddfd59)
">
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

 <img src="![out2](https://github.com/AbishekAnand15/COLOR_CONVERSIONS_OF-IMAGE/assets/118706942/c73c2cf6-65a1-41b9-94af-ef871e0a942f)
">
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

<img src="![out3](https://github.com/AbishekAnand15/COLOR_CONVERSIONS_OF-IMAGE/assets/118706942/541f079a-1dc0-4b1b-8623-53a4befe6eb5)
">
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
![Screenshot 2024-02-12 224411](https://github.com/srikarthickeyanganapathy/COLOR_CONVERSIONS_OF-IMAGE/assets/119393842/a0c420fa-5cd2-445f-a7e9-16297f6a2b3b)

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
![Screenshot 2024-02-12 224529](https://github.com/srikarthickeyanganapathy/COLOR_CONVERSIONS_OF-IMAGE/assets/119393842/ebc43a3c-a126-417c-a297-cc6307e45314)

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
![Screenshot 2024-02-12 224622](https://github.com/srikarthickeyanganapathy/COLOR_CONVERSIONS_OF-IMAGE/assets/119393842/36a0d7b2-1664-4624-83fb-5f0017ffab66)

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
![Screenshot 2024-02-12 224811](https://github.com/srikarthickeyanganapathy/COLOR_CONVERSIONS_OF-IMAGE/assets/119393842/e700495a-5cb4-45d6-8741-713cc5aa0497)

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
![Screenshot 2024-02-12 224924](https://github.com/srikarthickeyanganapathy/COLOR_CONVERSIONS_OF-IMAGE/assets/119393842/31196d0f-ffcd-4aac-b743-2d5caf54d037)

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







