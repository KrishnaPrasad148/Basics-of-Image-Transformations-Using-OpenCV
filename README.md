# Basics-of-Image-Transformations-Using-OpenCV

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the color image using imread().

### Step2:
Print the image using imshow().

### Step3:
Perform Translation, Scaling, Shearing on the image.

### Step4:
And perform Reflection, Rotation, Cropping on the image.

### Step5:
Display the output.

## Program:
```

Developed By: Krishna Prasad S
Register Number: 212223230108

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

### Original Image:
<img width="560" height="396" alt="orgnal" src="https://github.com/user-attachments/assets/29a5d2ce-8b84-4fcf-8587-073bb93b5c87" />

### i)Image Translation
<img width="560" height="336" alt="translated" src="https://github.com/user-attachments/assets/16494694-79bf-48d6-9e27-f380da6fa8c2" />


### ii) Image Scaling
<img width="560" height="231" alt="scaled" src="https://github.com/user-attachments/assets/f5dce4b5-01e5-4236-af09-3a8809de1cea" />


### iii)Image shearing
<img width="560" height="336" alt="sheared" src="https://github.com/user-attachments/assets/e1277a2a-a655-4643-91c9-3b0fc902a733" />



### iv)Image Reflection
<img width="989" height="360" alt="reflected" src="https://github.com/user-attachments/assets/c88890af-f86e-41c4-841c-83e117c68d97" />



### v)Image Rotation
<img width="515" height="372" alt="rotated" src="https://github.com/user-attachments/assets/dec497c1-e96a-4113-8621-92bf8dd1ea5b" />




### vi)Image Cropping
<img width="989" height="370" alt="cropped" src="https://github.com/user-attachments/assets/92221e25-f876-4a36-9f75-5c81fc151de6" />





## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
