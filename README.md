# BASIC-IMAGE-TRANSFORMATION


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br> Read the color image using imread().

### Step2:
<br> Print the image using imshow().

### Step3:
<br> Perform Translation, Scaling, Shearing on the image.

### Step4:
<br> And perform Reflection, Rotation, Cropping on the image.

### Step5:
<br> Display the output.

## Program:
```
Developed By: Prdaeep kumar G
Register Number: 212223230150
```

```python
i)Image Translation

tx, ty = 100, 200  # Translation factors (shift by 100 pixels horizontally and 50 vertically)
M_translation = np.float32([[1, 0, tx], [0, 1, ty]])  # Translation matrix: 

translated_image = cv2.warpAffine(image, M_translation, (2636, 1438))


ii) Image Scaling

fx, fy = 2.0, 1.0  
scaled_image = cv2.resize(image, None, fx=fx, fy=fy, interpolation=cv2.INTER_LINEAR)


iii)Image Shearing

shear_matrix = np.float32([[1, 0.5, 0], [0.5, 1, 0]])  
sheared_image = cv2.warpAffine(image, shear_matrix, (2636, 1438))


iv)Image Reflection

reflected_image = cv2.flip(image, 2)



v)Image Rotation

(height, width) = image.shape[:2]                                   # Get the image height and width
angle = 45                                                          # Rotation angle 
center = (width // 2, height // 2)  
M_rotation = cv2.getRotationMatrix2D(center, angle, 1)  

rotated_image = cv2.warpAffine(image, M_rotation, (width, height))  # Apply rotation



vi)Image Cropping

x, y, w, h = 0, 0, 2200, 1550  

cropped_image = image[y:y+h, x:x+w] 



```
## Output:

### Original image
<img width="774" height="511" alt="image" src="https://github.com/user-attachments/assets/e875bf96-1d5d-469d-be63-8d5a9a43420c" />

### i)Image Translation
<img width="767" height="432" alt="image" src="https://github.com/user-attachments/assets/e1dc3bed-e3e0-4b40-a265-78d62851205e" />


### ii) Image Scaling
<img width="783" height="296" alt="image" src="https://github.com/user-attachments/assets/693f5262-2b3e-4c93-bc74-7ed02b592e24" />



### iii)Image shearing
<img width="753" height="434" alt="image" src="https://github.com/user-attachments/assets/c19c900c-449d-41c4-9c3f-f7aaed58a2c9" />


### iv)Image Reflection
<img width="1245" height="457" alt="image" src="https://github.com/user-attachments/assets/0e8d654c-3510-47b1-a68c-602ecd5adcbf" />


### v)Image Rotation
<img width="662" height="467" alt="image" src="https://github.com/user-attachments/assets/d6b24ddc-4c82-43cd-8af2-dab7505b4c0f" />



### vi)Image Cropping
<img width="1318" height="466" alt="image" src="https://github.com/user-attachments/assets/651cdce1-b08b-474c-9368-a6e337de529b" />




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
