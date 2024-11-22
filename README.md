# IMAGE-TRANSFORMATIONS->

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import necessary libraries such as OpenCV, NumPy, and Matplotlib for image processing and visualization.

### Step2:
Read the input image using cv2.imread() and store it in a variable for further processing.

### Step3:
Apply various transformations like translation, scaling, shearing, reflection, rotation, and cropping by defining corresponding functions:

1.Translation moves the image along the x or y-axis.

2.Scaling resizes the image by scaling factors.

3.Shearing distorts the image along one axis.

4.Reflection flips the image horizontally or vertically. 5.Rotation rotates the image by a given angle.

### Step4:
Display the transformed images using Matplotlib for visualization. Convert the BGR image to RGB format to ensure proper color representation.

### Step5:
Save or display the final transformed images for analysis and use plt.show() to display them inline in Jupyter or compatible environments.
## Program:
```
Developed By:Pradeepraj P
Register Number: 212222240073

import cv2
import numpy as np
import matplotlib.pyplot as plt

# Load the image
image = cv2.imread('Ex4.jpeg')
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis('off')
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

i)Image Translation
# 1. Translation
rows, cols, _ = image.shape
M_translate = np.float32([[1, 0, 50], [0, 1, 100]])  # Translate by (50, 100) pixels
translated_image = cv2.warpAffine(image_rgb, M_translate, (cols, rows))
plt.imshow(translated_image)
plt.title("Translated Image")
plt.axis('off')

ii) Image Scaling
# 2. Scaling
scaled_image = cv2.resize(image_rgb, None, fx=1.5, fy=1.5, interpolation=cv2.INTER_LINEAR)
plt.imshow(scaled_image)
plt.title("Scaled Image")
plt.axis('off')

iii)Image shearing
# 3. Shearing
M_shear = np.float32([[1, 0.5, 0], [0.5, 1, 0]])  # Shear with factor 0.5
sheared_image = cv2.warpAffine(image_rgb, M_shear, (int(cols * 1.5), int(rows * 1.5)))
plt.imshow(sheared_image)
plt.title("Sheared Image")
plt.axis('off')

iv)Image Reflection
# 4. Reflection (Flip)
reflected_image = cv2.flip(image_rgb, 1)
plt.imshow(reflected_image)
plt.title("Reflected Image")
plt.axis('off')

v)Image Rotation
# 5. Rotation
M_rotate = cv2.getRotationMatrix2D((cols / 2, rows / 2), 45, 1)  # Rotate by 45 degrees
rotated_image = cv2.warpAffine(image_rgb, M_rotate, (cols, rows))
plt.imshow(rotated_image)
plt.title("Rotated Image")
plt.axis('off')

vi)Image Cropping
# 6. Cropping
cropped_image = image_rgb[50:300, 100:200]
plt.figure(figsize=(4, 4))
plt.imshow(cropped_image)
plt.title("Cropped Image")
plt.axis('off')
plt.show()

```
## Output:
### Original image
![image](https://github.com/user-attachments/assets/1e1f9a26-01ad-47a6-9699-920409c1ae74)

### i)Image Translation
![download](https://github.com/user-attachments/assets/56d5c127-5052-4e44-ae10-6f3c8004ff99)

### ii) Image Scaling
![download](https://github.com/user-attachments/assets/8b0d6897-113f-40c6-96db-0604b582f79e)

### iii)Image shearing
![download](https://github.com/user-attachments/assets/d3bd0e32-f3b1-4cba-ac28-f8087d06bde2)

### iv)Image Reflection
![download](https://github.com/user-attachments/assets/7b87f108-d9c2-47a7-ae70-aab2fb310520)

### v)Image Rotation
![download](https://github.com/user-attachments/assets/c83ad832-d140-41c2-96b2-16bbfefd9e23)


### vi)Image Cropping
![download](https://github.com/user-attachments/assets/9e0fca08-2c38-4690-a471-f750601d3c10)

## Result: 
Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
