# THRESHOLDING
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1:
Load the necessary packages.

### Step2:
Read the Image and convert to grayscale.

### Step3:
Use Global thresholding to segment the image.

### Step4:
Use Adaptive thresholding to segment the image.

### Step5:
Use Otsu thresholding to segment the image.

### Step6:
Display the result

## Program
```
NAME : JAYAKRISHNAN L B L
REGISTER NUMBER : 212222230052
```

### Load the necessary packages
```
import cv2
import matplotlib.pyplot as plt

```


### Read the Image and convert to grayscale
```
image = cv2.imread("flower.jpg", 0)
```


### Use Global thresholding to segment the image
```
 global_threshold = cv2.threshold(image, 128, 255, cv2.THRESH_BINARY)
```


### Use Adaptive thresholding to segment the image
```
adaptive_threshold = cv2.adaptiveThreshold(image, 255, cv2.ADAPTIVE_THRESH_MEAN_C, cv2.THRESH_BINARY, 11, 2)
```


### Use Otsu's method to segment the image 

```
 otsu_threshold = cv2.threshold(image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)
```


### Display the results
```
plt.figure(figsize=(18, 6))

plt.imshow(image, cmap='gray')
plt.title("Original Image")
plt.axis("off")

plt.imshow(global_threshold, cmap='gray')
plt.title("Global Thresholding")
plt.axis("off")

plt.imshow(adaptive_threshold, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis("off")

plt.imshow(otsu_threshold, cmap='gray')
plt.title("Otsu's Thresholding")
plt.axis("off")

plt.show()

```
## Output

### Original Image
![image](https://github.com/Jayakrishnan22003251/THRESHOLDING/assets/120232371/48e8fdab-5640-4933-a639-1f48a582d7f6)



### Global Thresholding
![image](https://github.com/Jayakrishnan22003251/THRESHOLDING/assets/120232371/6896f3f9-95bb-45e8-afb3-dbffb41601e1)



### Adaptive Thresholding
![image](https://github.com/Jayakrishnan22003251/THRESHOLDING/assets/120232371/e38777bc-7cf7-4cd7-8073-2a8131f9cbe5)



### Optimum Global Thesholding using Otsu's Method
![image](https://github.com/Jayakrishnan22003251/THRESHOLDING/assets/120232371/9f5ad4a5-4fad-4d1e-981d-b6a9135fd0dd)




## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.

