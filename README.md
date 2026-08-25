# Exp-9--Record-IMPLEMENTATION-OF-EROSION-AND-DILATION
# Implementation of Erosion and Dilation Using OpenCV
## Developed By

**Name:** AJITH KUMAR A

**Register No:** 212223230009

## Aim

To write a Python program using OpenCV to perform morphological operations such as Erosion and Dilation on an image.

The program performs the following operations:

- Image Erosion
- Image Dilation

## Software Used

- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (cv2)
- NumPy
- Matplotlib

## Algorithm

### Step 1:

Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:

Create a blank image using NumPy.

### Step 3:

Insert text onto the image using OpenCV's text drawing function.

### Step 4:

Display the original image.

### Step 5:

Create a structuring element (kernel) of suitable size.

### Step 6: Image Erosion

- Apply the erosion operation using the created kernel.
- Remove pixels from the boundaries of foreground objects.
- Display the eroded image.

### Step 7: Image Dilation

- Apply the dilation operation using the same kernel.
- Add pixels to the boundaries of foreground objects.
- Display the dilated image.

### Step 8:

Compare the original, eroded, and dilated images.

## Program and Output

### Original Image
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("ajith photo.jpeg")
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.title("Original Image")
plt.axis("off")
plt.show()
```
<img width="347" height="462" alt="image" src="https://github.com/user-attachments/assets/c64a00ed-bbdd-4c55-a4d9-75831385e454" />


### Erosion
```
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
erosion = cv2.erode(img, kernel, iterations=1)
plt.imshow(erosion, cmap="gray")
plt.title("Image Erosion")
plt.axis("off")
plt.show()
```

<img width="362" height="462" alt="image" src="https://github.com/user-attachments/assets/0734dd3d-a45e-43bf-b612-dca8dd1750ea" />



### Dilation
```
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
dilation = cv2.dilate(img, kernel, iterations=1)
plt.imshow(dilation, cmap="gray")
plt.title("Image Dilation")
plt.axis("off")
plt.show()
```
<img width="377" height="457" alt="image" src="https://github.com/user-attachments/assets/52bf3270-e8db-45c5-8377-b12a3530699b" />




## Result

Thus, the morphological operations **Erosion** and **Dilation** are successfully implemented using OpenCV.
