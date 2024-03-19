# IMPLEMENTATION-OF-FILTERS
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the required libraries.

### Step2
Convert the image from BGR to RGB.

### Step3
Apply the required filters for the image separately.

### Step4
Plot the original and filtered image by using matplotlib.pyplot

### Step5
End the program.


## Program:
#### Developed By   : SRI KARTHICKEYAN GANAPATHY
#### Register Number: 212222240102
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("space.jpeg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()
```
ii) Using Weighted Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("space.jpeg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()
```
iii) Using Gaussian Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("space.jpeg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```

iv) Using Median Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("space.jpeg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()
```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("space.jpeg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()
```
ii) Using Laplacian Operator
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("space.jpeg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()
```

## OUTPUT:
### 1. Smoothing Filters

#### i) Using Averaging Filter
![image](https://github.com/srikarthickeyanganapathy/Implementation-of-filter/assets/119393842/c557ce01-0395-4ea7-be38-564e9ddd8f4c)

#### ii) Using Weighted Averaging Filter
![download](https://github.com/srikarthickeyanganapathy/Implementation-of-filter/assets/119393842/5a48baf6-f469-4869-aeac-1b41a4a22ba6)

#### iii) Using Gaussian Filter
![download](https://github.com/srikarthickeyanganapathy/Implementation-of-filter/assets/119393842/1fb73acb-2404-4a0d-af6f-8619b072a907)

#### iv) Using Median Filter
![download](https://github.com/srikarthickeyanganapathy/Implementation-of-filter/assets/119393842/4dd1dbcd-ce2c-41a9-ba11-00b7960a6671)

### 2. Sharpening Filters

#### i) Using Laplacian Kernal
![download](https://github.com/srikarthickeyanganapathy/Implementation-of-filter/assets/119393842/f9e20a7c-5e66-4780-b127-a94fba1b6231)

#### ii) Using Laplacian Operator
![download](https://github.com/srikarthickeyanganapathy/Implementation-of-filter/assets/119393842/3a686a08-9413-4657-92c2-68067f8b77b7)

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
