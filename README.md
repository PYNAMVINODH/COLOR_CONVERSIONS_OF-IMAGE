# COLOR_CONVERSIONS_OF-IMAGE
## AIM:
To write a python program using OpenCV to do the following image manipulations.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
```
1. Read and Display an Image:

Load an image from your local directory and display it.

2. Draw Shapes and Add Text:

Draw a line from the top-left to the bottom-right of the image.

Draw a circle at the center of the image.

o Draw a rectangle around a specific region of interest in the image.

Add the text "OpenCV Drawing" at the top-left corner of the image.

3. Image Color Conversion:

Convert the image from RGB to HSV and display it.

Convert the image from RGB to GRAY and display it.

O Convert the image from RGB to YCrCb and display it.

Convert the HSV image back to RGB and display it.

4. Access and Manipulate Image Pixels:

Access and print the value of the pixel at coordinates (100, 100). Modify the color of the pixel at (200, 200) to white.

5. Image Resizing:

Resize the original image to half its size and display it.

6. Image Cropping:

Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.

7. Image Flipping:

Flip the original image horizontally and display it.

Flip the original image vertically and display it.

8. Write and Save the Modified Image:

Save the final modified image to your local directory.
```

# Program:
```
Developed By: PYNAM VINODH
Register Number: 212223240131
```


### 1.) Read and display the image

```Python
import cv2
img = cv2.imread("lokesh.jpg")
res = cv2.line(img, (0, 0), (599, 799), (200, 100, 205), 10)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()

``` 
 

### OUTPUT:

![image](https://github.com/user-attachments/assets/4c500e7b-1a78-4672-a8a2-aeb3f3710ebf)


 

### 2.) Draw Shapes and Add Text:
i)Draw a line from the top-left to the bottom-right of the image.

```Python
import cv2
img = cv2.imread("lokesh.jpg")
res = cv2.line(img, (0, 0), (599, 799), (200, 100, 205), 10)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()


```


### OUTPUT:

![image](https://github.com/user-attachments/assets/fa563f7d-311c-40a2-9830-981af61e1b66)



 
### ii)Draw a circle at the center of the image.
```Python
import cv2

# Load the image
img = cv2.imread("lokesh.jpg")

# Get the dimensions of the image
height, width, _ = img.shape

# Calculate the center of the image
center_coordinates = (width // 2, height // 2)

# Draw a circle at the center of the image
res = cv2.circle(img, center_coordinates, 150, (255, 0, 0), 10)

# Display the image with the circle
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()



```


### OUTPUT:
![image](https://github.com/user-attachments/assets/41d114c8-453b-4162-afa8-74b80db283a6)




      
### iii)Draw a rectangle around a specific region of interest in the image.
```Python
import cv2

img = cv2.imread("lokesh.jpg")
start=(0,0)
stop=(409,529)
color=(100,255,100)
thickness=10
res_img=cv2.rectangle(img,start,stop,color,thickness)
# Display the HSV image
cv2.imshow('Image Window', res_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
 

### OUTPUT:

![image](https://github.com/user-attachments/assets/d8625052-38ee-46fc-a709-4af53bc6a2bc)



      
### iv)Add the text "OpenCV Drawing" at the top-left corner of the image.

 ```Python
import cv2

# Load the image
img = cv2.imread("lokesh.jpg")

# Define the text to be added and its position
text = "OPENCV DRAWING"
position = (50, 50)  # Positioning the text at the top-left corner

# Set the font, scale, color, and thickness of the text
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (255, 255, 255)  # White color
thickness = 2

# Add the text to the image
res = cv2.putText(img, text, position, font, font_scale, color, thickness, cv2.LINE_AA)

# Display the image with the text
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()




```

    
### OUTPUT:

![image](https://github.com/user-attachments/assets/c08b3f56-0e63-43b2-9689-899cc05dfb4d)




### 3.)Image Color Conversion:
i)Convert the image from RGB to HSV and display it.
```Python
import cv2
img = cv2.imread('lokesh.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![image](https://github.com/user-attachments/assets/5520ea70-3575-4811-bf24-5ae1de8277bc)


#### ii.)Convert the image from RGB to GRAY and display it.
```Python
import cv2
img = cv2.imread('lokesh.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### Output:
![image](https://github.com/user-attachments/assets/07e56ace-657b-42da-a150-fe628ba9e3b7)


#### iii.)Convert the image from RGB to YCrCb and display it.
```Python
import cv2
img = cv2.imread('lokesh.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
cv2.waitKey(0)
cv2.destroyAllWindows()



```
### Output:
![image](https://github.com/user-attachments/assets/2b6fbb2b-66be-4510-9712-575b3692d76a)

#### iv.)Convert the HSV image back to RGB and display it.
```Python
import cv2
img = cv2.imread('lokesh.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Output:
![image](https://github.com/user-attachments/assets/697153f8-72b9-41eb-8793-3a0c60be9c48)

## 4. Access and Manipulate Image Pixels:
```Python
import cv2

# Load and resize the image
img = cv2.imread('lokesh.jpg', 1)
img = cv2.resize(img, (300, 200))

# Show the original image
cv2.imshow('Original Image', img)

# 1. Access and print the value of the pixel at coordinates (100, 100)
pixel_value = img[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")

# 2. Modify the color of the pixel at (199, 199) to white
img[199, 199] = [255, 255, 255]  # Setting the pixel value to white (BGR)

# Display the modified image
cv2.imshow('Modified Image', img)

# Wait for a key press and close the windows
cv2.waitKey(0)
cv2.destroyAllWindows()




```
### Output:
![image](https://github.com/user-attachments/assets/133ca317-fb2b-4d03-ab4f-8ac6de69787d)


![image](https://github.com/user-attachments/assets/29b7bad7-059e-470e-ac8e-eb88603e4b7c)


## 5. Image Resizing:
```Python
width=600
height=800
half_width=300
half_height=400
resized_img = cv2.resize(image, (300, 400))
cv2.imshow('Original',image)
cv2.imshow('resized',resized_img)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
### Output:
![image](https://github.com/user-attachments/assets/c084d3d6-ed7c-4eb6-a6f9-2604b17d75b5)

## 6.Image Cropping:
```Python
import cv2

# Load the image
image1=cv2.imread('lokesh.jpg',1)

# Define the starting point and size of the ROI
x, y = 50, 50
width, height = 100, 100

# Crop the ROI
roi = image1[y:y + height, x:x + width]

# Display the cropped ROI
cv2.imshow('Cropped Image', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Output:
![image](https://github.com/user-attachments/assets/5116cfb9-8d92-40a8-917e-a49bbde56444)


## 7.Image Flipping:
i.)Flip the original image horizontally and display it.
```Python


import cv2
img = cv2.imread("lokesh.jpg")
img = cv2.resize(img,(300,200))
res=cv2.rotate(img,cv2.ROTATE_180)
cv2.imshow('Original',img)
cv2.imshow('Rotate Image', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Output:
![image](https://github.com/user-attachments/assets/1481174a-a019-40e8-93ca-282a99c53721)



#### ii.)Flip the original image vertically and display it.

```Python
import cv2

img = cv2.imread("lokesh.jpg")
img = cv2.resize(img,(300,200))
res=cv2.rotate(img,cv2.ROTATE_90_CLOCKWISE)
# Display the HSV image
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()



```
### Output:
![image](https://github.com/user-attachments/assets/be1f291b-7d1d-4857-9bbf-ec85f38ef080)


## 8. Write and Save the Modified Image:
```Python
import cv2
img = cv2.imread("lokesh.jpg")
img = cv2.resize(img,(300,200))
cv2.imwrite('lokesh1.jpg',img)
```
### Output:
![image](https://github.com/user-attachments/assets/2e75dcf5-d117-4d2f-9d55-bd657e187306)

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.
