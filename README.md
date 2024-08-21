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
Developed By: PYNAM VINODH
Register Number: 212223240131
```
<table>
  <tr>
    <td width=50%>

### i) Read and display the image
```Python
    import cv2
    image=cv2.imread('07.jpg',1)
    image=cv2.resize(image,(400,300))
    cv2.imshow('JESHWANTH KUMAR',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
``` 
  </td>
  <td>

### OUTPUT:

![image](https://github.com/user-attachments/assets/a68518c2-2c30-4dbb-924c-4ced678e03fa)

  </td>
  </tr>

   <tr>
    <td width=50%>

### ii)Write the image
```Python
     import cv2
    image=cv2.imread('07.jpg',0)
    cv2.imwrite('DEMO07.jpg',image)
```
  </td>
  <td>

### OUTPUT:

![image](https://github.com/user-attachments/assets/bc3cba66-83c1-46a1-9afa-df8e5b2211f9)



  </td>
  </tr>
  <tr>
    <td width=50%>

### iii)Shape of the Image
```Python
     import cv2
    image=cv2.imread('07.jpg',1)
    print(image.shape)
```
  </td>
  <td>

### OUTPUT:
![image](https://github.com/user-attachments/assets/cbb90037-71b9-407e-8204-de5a619d7803)



  </td>
  </tr>
  <tr>
    <td>
      
### iv)Access rows and columns
```Python
import random
import cv2
image=cv2.imread('07.jpg',1)
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

![image](https://github.com/user-attachments/assets/5d7a2f54-e4cc-437c-a026-972fd5b073a7)



  </td>
  </tr>
  <tr>
    <td width=50%>
      
### v)Cut and paste portion of image

 ```Python
 import cv2
image=cv2.imread('07.jpg',1)
image=cv2.resize(image,(400,400))
tag =image[130:200,110:190]
image[110:180,120:200] = tag
cv2.imshow('PartImage1',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
  </td>
  <td>
    
### OUTPUT:

![image](https://github.com/user-attachments/assets/de28c346-2b01-4730-ac57-39be4dd01eec)


  </td>
  </tr>
</table>

### vi) BGR and RGB to HSV and GRAY
```Python
import cv2
img = cv2.imread('07.jpg',1)
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
![image](https://github.com/user-attachments/assets/eb59843d-857a-4071-9d39-e0bac7c14809)


![image](https://github.com/user-attachments/assets/cb0c72b3-90e4-4052-88c3-0dcf1160ab4d)



![image](https://github.com/user-attachments/assets/9e488725-d389-4c1a-8bd1-231ef140664b)


![image](https://github.com/user-attachments/assets/8bd5c721-0f97-4098-8cb8-1abf6bfe7deb)


![image](https://github.com/user-attachments/assets/9c76db52-10c9-4eaf-910b-3374ee9e95a3)





### vii) HSV to RGB and BGR
```Python
import cv2
img = cv2.imread('07.jpg')
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
![image](https://github.com/user-attachments/assets/c3034453-96c6-4890-be86-b2fb3b73ff1e)


![image](https://github.com/user-attachments/assets/f6c599eb-d834-4281-9b8f-716f067ea175)


![image](https://github.com/user-attachments/assets/c8980aa7-0a99-4590-911d-f09c286caa03)



### viii) RGB and BGR to YCrCb
```Python
import cv2
img = cv2.imread('07.jpg')
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
![image](https://github.com/user-attachments/assets/fdce1b45-c15b-4e10-ac48-b39e3eb27aaa)

![image](https://github.com/user-attachments/assets/2ef20500-19ee-4144-86c7-a0523f2b6fdb)

![image](https://github.com/user-attachments/assets/bd0c3c0d-7d2a-45b2-bce3-8439b576c01c)



### ix) Split and merge RGB Image
```Python
import cv2
img = cv2.imread('07.jpg',1)
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
cv2.destroyAllWindows()
```

### OUTPUT:
![image](https://github.com/user-attachments/assets/8f98ff5a-eb18-4474-bb50-1ab563fad6b2)


![image](https://github.com/user-attachments/assets/7baf449e-adc1-4600-88f1-87536fc177f6)


![image](https://github.com/user-attachments/assets/ccaa2bb6-875e-4db6-af43-471e00f8a7b4)

![image](https://github.com/user-attachments/assets/47c7b756-3e2b-4813-a5ec-8d6d003547a7)





### x) Split and merge HSV Image
```Python
import cv2
img = cv2.imread('07.jpg',1)
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
![image](https://github.com/user-attachments/assets/7cbd5afe-795f-4638-ab2a-3d61877d1e6f)

![image](https://github.com/user-attachments/assets/ed73d9b8-8f8e-4bf3-b7b2-92a5343e229f)

![image](https://github.com/user-attachments/assets/aebf3c52-e727-4c54-8b5a-990f6f04ff67)

![image](https://github.com/user-attachments/assets/b181c598-1895-4a21-9c7e-637485705eb4)




## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.
