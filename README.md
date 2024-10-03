# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>Import all the necessary modules

### Step2:
<br>Choose an image and save it as filename.jpg

### Step3:
<br>Use imread to read the image

### Step4:
<br>Use cv2.warpPerspective(image,M,(cols,rows)) to translation the image

### Step5:
<br>Use cv2.warpPerspective(image,M,(cols*2,rows*2)) to scale the image
### Step6:
Use cv2.warpPerspective(image,M,(int(cols*1.5),int(rows*1.5))) for x and y axis to shear the image

### Step7:
<br>Use cv2.warpPerspective(image,M,(int(cols),int(rows))) for x and y axis to reflect the image
### Step8:
<br>Use cv2.warpPerspective(image,M,(int(cols),int(rows))) to rotate the image
### Step9:
<br>Crop the image to remove unwanted areas from an image
### Step10:

<br>Use cv2.imshow to show the image
### Step11:
<br>End the program
## Program:

## Developed By: Jeyabalan T
# Register Number: 212222240040
i)Image Translation
```python

import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread("dip.jpg")
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M=np.float32([[1,0,100],[0,1,200],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
print("Image Translation:")
plt.imshow(translated_image)
plt.show()

```


ii) Image Scaling
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('dip.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M=np.float32([[1.5,0,0],[0,1.8,0],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols*2,rows*2))
plt.axis('off')
print("Image Scaling:")
plt.imshow(translated_image)
plt.show()
```


iii)Image shearing
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('dip.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M1=np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M2=np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
translated_image1=cv2.warpPerspective(input_image,M1,(int(cols*1.5),int(rows*1.5)))
translated_image2=cv2.warpPerspective(input_image,M2,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
print("Image Shearing:")
plt.imshow(translated_image1)
plt.imshow(translated_image2)
plt.show()
```

iv)Image Reflection
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('dip.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M1=np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M2=np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
translated_image1=cv2.warpPerspective(input_image,M1,(int(cols),int(rows)))
translated_image2=cv2.warpPerspective(input_image,M2,(int(cols),int(rows)))
plt.axis('off')
print("Image Reflection:")
plt.imshow(translated_image1)
plt.imshow(translated_image2)
plt.show()
```


v)Image Rotation
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('dip.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M1=np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M2=np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
translated_image1=cv2.warpPerspective(input_image,M1,(int(cols),int(rows)))
translated_image2=cv2.warpPerspective(input_image,M2,(int(cols),int(rows)))
plt.axis('off')
print("Image Reflection:")
plt.imshow(translated_image1)
plt.imshow(translated_image2)
```


vi)Image Cropping
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('dip.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(int(cols),int(rows)))
plt.axis('off')
print("Image Cropping:")
plt.imshow(translated_image)
plt.show()
```




## Output:
 i)Image Translation

![image](https://github.com/user-attachments/assets/d06ec821-2ec0-4408-8fdf-907b850ef631)





 ii) Image Scaling

![image](https://github.com/user-attachments/assets/82596a35-14bf-46f8-b6e0-43f59ac8b3a6)





 iii)Image shearing

![image](https://github.com/user-attachments/assets/91df7a87-96a4-4fe0-a9fa-af4027af48cc)






 iv)Image Reflection

![image](https://github.com/user-attachments/assets/1cf1fd0a-c1d0-4afd-8252-0bbcf7383ce2)






 v)Image Rotation

![image](https://github.com/user-attachments/assets/3dfa64cf-68ba-4b6c-a001-54f1dcca9e45)






vi)Image Cropping

![image](https://github.com/user-attachments/assets/a7e8bab2-d511-4c7c-831b-bc64bd1c3b18)








## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
