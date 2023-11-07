# IMPLEMENTATION-OF-FILTERSS
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
Step1
Read and show the image

Step2
Apply the filtering technique that we want to perform

Step3
Show the filtered image

## Program:
```
 Developed By   :G.Lutheesh
 Register Number:212221230029
```

### 1. Smoothing Filters

i) Using Averaging Filter
```
import cv2
import numpy as np
image = cv2.imread("ya.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
cv2.imshow('original',original_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
kernel1 = np.ones((11,11),np.float32)/121
box_filter = cv2.filter2D(original_image,-1,kernel1)
cv2.imshow('box_filter',box_filter)
cv2.waitKey(0)
cv2.destroyAllWindows()




```
ii) Using Weighted Averaging Filter
```
import cv2
import numpy as np
image = cv2.imread("ya.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
cv2.imshow('original',original_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
kernel2 = np.array([[1,2,1],[2,4,2],[1,2,1]])/16
weighted_filter = cv2.filter2D(original_image,-1,kernel2)
cv2.imshow('weighted_filter',weighted_filter)
cv2.waitKey(0)
cv2.destroyAllWindows()








```
iii) Using Gaussian Filter
```
import cv2
import numpy as np
image = cv2.imread("ya.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
cv2.imshow('original',original_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
gaussian_blur = cv2.GaussianBlur(src = original_image, ksize = (11,11), sigmaX=0,
sigmaY=0)
cv2.imshow('gaussian_filter',gaussian_blur)
cv2.waitKey(0)
cv2.destroyAllWindows()





```

iv) Using Median Filter
```
import cv2
import numpy as np
image = cv2.imread("ya.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
cv2.imshow('original',original_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
median = cv2.medianBlur(src=original_image,ksize = 11)
cv2.imshow('median_filter',median)
cv2.waitKey(0)
cv2.destroyAllWindows()





```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```
import cv2
import numpy as np
image = cv2.imread("ya.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
cv2.imshow('original',original_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
kernel3 = np.array([[0,1,0],[1,-4,1],[0,1,0]])
laplacian_kernel = cv2.filter2D(original_image,-1,kernel3)
cv2.imshow('laplacian_kernel',laplacian_kernel)
cv2.waitKey(0)
cv2.destroyAllWindows()





```
ii) Using Laplacian Operator
```
import cv2
import numpy as np
image = cv2.imread("ya.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
cv2.imshow('original',original_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
laplacian_operator = cv2.Laplacian(original_image,cv2.CV_64F)
cv2.imshow('laplacian_operator',laplacian_operator)
cv2.waitKey(0)
cv2.destroyAllWindows()






```

## OUTPUT:
### 1. Smoothing Filters
![image](https://github.com/Lutheeshgoparapu/IMPLEMENTATION-OF-FILTERSS/assets/94154531/95a06700-3a07-4b20-b81b-3576c5457de8)


#### i) Using Averaging Filter
![image](https://github.com/Lutheeshgoparapu/IMPLEMENTATION-OF-FILTERSS/assets/94154531/20db831e-9d5c-4b6f-ac32-877004bda40c)


#### ii) Using Weighted Averaging Filter

![image](https://github.com/Lutheeshgoparapu/IMPLEMENTATION-OF-FILTERSS/assets/94154531/7f683566-d228-408d-8665-299a8bab356c)

#### iii) Using Gaussian Filter

![image](https://github.com/Lutheeshgoparapu/IMPLEMENTATION-OF-FILTERSS/assets/94154531/dacc202f-0f0d-4f5e-ade1-12c0235bc3c8)

#### iv) Using Median Filter
![image](https://github.com/Lutheeshgoparapu/IMPLEMENTATION-OF-FILTERSS/assets/94154531/8e6245b1-4034-4de8-bb2e-95bdaeba21b1)


### 2. Sharpening Filters
</br>

#### i) Using Laplacian Kernal
![image](https://github.com/Lutheeshgoparapu/IMPLEMENTATION-OF-FILTERSS/assets/94154531/c8e4e6e9-8e09-45f9-a105-410b8da3cea5)


#### ii) Using Laplacian Operator
![image](https://github.com/Lutheeshgoparapu/IMPLEMENTATION-OF-FILTERSS/assets/94154531/4be421aa-9cc9-4199-8996-4c071d3948c5)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
