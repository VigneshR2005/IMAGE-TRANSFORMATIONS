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



## Program:

Developed By: R Vignesh

Register Number: 212222230172

i)Image Translation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("dog.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(in_img)
plt.show()
```
ii) Image Scaling
```import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("dog.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M=np.float32([[1,0,50],
              [0,1,50],
              [0,0,1]])
trans_img=cv2.warpPerspective(in_img, M, (cols,rows))
plt.axis('off')
plt.imshow(trans_img)
plt.show()
```
iii)Image shearing
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("dog.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M_x=np.float32([[1,0.5,0],
                [0,1 ,0],
                [0,0 ,1]])
M_y=np.float32([[1,  0,0],
                [0.5,1,0],
                [0,  0,1]])
sheared_img_x=cv2.warpPerspective(in_img,M_x,(int(cols),int(rows)))
sheared_img_y=cv2.warpPerspective(in_img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(sheared_img_x)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_y)
plt.show()
```
iv)Image Reflection
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("dog.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M_x=np.float32([[1,  0,0  ],
                [0,-1,rows],
                [0,0,1  ]])
M_y=np.float32([[-1,0,cols],
                [ 0,1,0  ],
                [ 0,0,1  ]])
reflect_x=cv2.warpPerspective(in_img,M_x,(int(cols),int(rows)))
reflect_y=cv2.warpPerspective(in_img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflect_x)
plt.show()
plt.axis('off')
plt.imshow(reflect_y)
plt.show()  
```
v)Image Rotation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("dog.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
              [np.sin(angle),np.cos(angle),0],
              [0,0,1]])
rotated_img=cv2.warpPerspective(in_img,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()  
```
vi)Image Cropping
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img = cv2.imread("dog.jpg")
in_img = cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
plt.imshow(in_img)
plt.show()
cropped_img=in_img[10:150 ,10:250]
plt.imshow(cropped_img)
plt.show()
```
## Output:
### i)Image Translation

![Screenshot 2024-10-01 113500](https://github.com/user-attachments/assets/b2f60924-a5ea-42fd-99b7-97ac81aa5b12)



### ii) Image Scaling
![download](https://github.com/user-attachments/assets/7b468d04-2d5b-4ab7-adff-18156e43251d)




### iii)Image shearing
![download](https://github.com/user-attachments/assets/876238f3-cbeb-4a03-a9c1-a904ef7666bc)
![download](https://github.com/user-attachments/assets/4022d058-37bc-4a9e-b28e-b4616aeca35b)



### iv)Image Reflection

![download](https://github.com/user-attachments/assets/0b79f629-4614-4c28-b8ff-50ba06de5cdb)

![download](https://github.com/user-attachments/assets/c0a3fbe5-973d-49c4-ab41-e4dc82d531ff)





### v)Image Rotation
![download](https://github.com/user-attachments/assets/6d8c6154-0ca4-44bf-a5af-b7542c8e0ae5)



### vi)Image Cropping
![download](https://github.com/user-attachments/assets/ab43066c-55e0-4bde-82e2-9449020c69ef)

Original

![download](https://github.com/user-attachments/assets/b40f2573-7043-4929-acfc-4efdffcc5f9e)

Cropped

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
