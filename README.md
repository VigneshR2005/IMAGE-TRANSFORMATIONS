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


### i)Image Translation

![download](https://github.com/user-attachments/assets/76de5944-29e7-4748-a8e9-8c1227407e2d)




### ii) Image Scaling

![download](https://github.com/user-attachments/assets/84ba7c44-35a0-40ab-b870-e5fc19308bb9)





### iii)Image shearing

![download](https://github.com/user-attachments/assets/07e8df97-96bb-40a9-ba34-94a4fce8dc7a)


![download](https://github.com/user-attachments/assets/6366a811-401f-4d09-b5d9-bdb628eef075)


### iv)Image Reflection

![download](https://github.com/user-attachments/assets/ffa3562e-467b-45f7-970c-b18429a53dd1)



![download](https://github.com/user-attachments/assets/0a86c458-74d6-420b-a65f-e55289bca722)





### v)Image Rotation

![download](https://github.com/user-attachments/assets/2288c9a8-e862-4ded-a121-5e15880b3fdf)



### vi)Image Cropping
orginal
![download](https://github.com/user-attachments/assets/701637d5-810f-4bae-84aa-add047008263)


Cropped
![download](https://github.com/user-attachments/assets/7312f517-e290-4e67-80a9-ef7804837cb1)



## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
