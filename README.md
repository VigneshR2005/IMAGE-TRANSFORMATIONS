# IMAGE TRANSFORMATION

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages.

### Step2:
Load the image file in the program.

### Step3:
Use the techniques for Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

### Step4
Display the modified image output.

### Step5:
End the program.


```
## Program:

Developed By: R Vignesh

Register Number: 212222230172

i)Image Translation
import cv2
import numpy as np

# Load the image
image = cv2.imread('dog.jpg')

# Define translation matrix: (shift along x, shift along y)
tx, ty = 100, 50
translation_matrix = np.float32([[1, 0, tx], [0, 1, ty]])

# Apply translation
translated_image = cv2.warpAffine(image, translation_matrix, (image.shape[1], image.shape[0]))

# Display
cv2.imshow('Translated Image', translated_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

ii) Image Scaling
# Scaling factors
scale_x, scale_y = 1.5, 1.5

# Resize image
scaled_image = cv2.resize(image, None, fx=scale_x, fy=scale_y, interpolation=cv2.INTER_LINEAR)

# Display
cv2.imshow('Scaled Image', scaled_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

iii)Image shearing
# Define shearing matrix
shear_factor = 0.5
shearing_matrix = np.float32([[1, shear_factor, 0], [0, 1, 0]])

# Apply shearing
sheared_image = cv2.warpAffine(image, shearing_matrix, (int(image.shape[1] * 1.5), image.shape[0]))

# Display
cv2.imshow('Sheared Image', sheared_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

iv)Image Reflection
 Reflection_Image= cv2.flip(image, 1)

# Display
cv2.imshow('Reflection Image', Reflection_Image)
cv2.waitKey(0)
cv2.destroyAllWindows()

v)Image Rotation
# Rotation center, angle and scale
center = (image.shape[1] // 2, image.shape[0] // 2)
angle, scale = 45, 1.0

# Get rotation matrix
rotation_matrix = cv2.getRotationMatrix2D(center, angle, scale)

# Apply rotation
rotated_image = cv2.warpAffine(image, rotation_matrix, (image.shape[1], image.shape[0]))

# Display
cv2.imshow('Rotated Image', rotated_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

vi)Image Cropping
# Define the region of interest (ROI)
x, y, w, h = 100, 100, 300, 300
cropped_image = image[y:y+h, x:x+w]

# Display
cv2.imshow('Cropped Image', cropped_image)
cv2.waitKey(0)
cv2.destroyAllWindows()



```
## Output:

### Original:

![download](https://github.com/user-attachments/assets/b40f2573-7043-4929-acfc-4efdffcc5f9e)

### i)Image Translation

![Screenshot 2024-11-18 190813](https://github.com/user-attachments/assets/a5bffeb3-5f69-4f34-bcfa-9402109bfe94)




### ii) Image Scaling
![download](https://github.com/user-attachments/assets/7b468d04-2d5b-4ab7-adff-18156e43251d)




### iii)Image shearing
![download](https://github.com/user-attachments/assets/876238f3-cbeb-4a03-a9c1-a904ef7666bc)
![download](https://github.com/user-attachments/assets/4022d058-37bc-4a9e-b28e-b4616aeca35b)



### iv)Image Reflection

![download](https://github.com/user-attachments/assets/c0a3fbe5-973d-49c4-ab41-e4dc82d531ff)

![download](https://github.com/user-attachments/assets/0b79f629-4614-4c28-b8ff-50ba06de5cdb)







### v)Image Rotation
![download](https://github.com/user-attachments/assets/6d8c6154-0ca4-44bf-a5af-b7542c8e0ae5)



### vi)Image Cropping
![Screenshot 2024-11-18 191550](https://github.com/user-attachments/assets/8b5c5748-16f3-48b6-81ca-8b3d5eb308ed)


Cropped

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
