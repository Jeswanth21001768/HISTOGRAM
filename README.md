# HISTOGRAM
# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Load the image using a suitable library like OpenCV.

### Step2:
Convert the image to grayscale using cvtColor() if needed.

### Step3:
Calculate the histogram using calcHist() and plot it with Matplotlib.

### Step4:
Perform histogram equalization using equalizeHist() for enhanced contrast.

### Step5:
Visualize results by plotting histograms and displaying original and equalized images side by side.


## Program:
```python
# Developed By: Jeswanth.S
# Register Number: 212221230042
```


# Write your code to find the histogram of the grayscale image and color image channels.
```
import cv2
import matplotlib.pyplot as plt
import cv2
import numpy as np
import matplotlib.pyplot as plt
image_path = 't.jpg'
gray_image = cv2.imread(image_path, cv2.IMREAD_GRAYSCALE)
hist = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
plt.plot(hist)
plt.xlabel('Pixel Value')
plt.ylabel('Frequency')
plt.title('Histogram of Grayscale Image')
plt.show()
```
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

#### Load a color image
image_path = 'M.jpg'
color_image = cv2.imread(image_path, cv2.IMREAD_COLOR)

#### Convert color image to grayscale
gray_image = cv2.cvtColor(color_image, cv2.COLOR_BGR2GRAY)

#### Calculate histogram
hist = cv2.calcHist([gray_image], [0], None, [256], [0, 256])

#### Plot the histogram
plt.plot(hist)
plt.xlabel('Pixel Value')
plt.ylabel('Frequency')
plt.title('Histogram of color Image')
plt.show()
```

# Display the histogram of the grayscale image and any one-channel histogram from the color image
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

#### Load a grayscale image
image_path = 'G.jpg'
gray_image = cv2.imread(image_path, cv2.IMREAD_GRAYSCALE)

#### Calculate histogram
hist = cv2.calcHist([gray_image], [0], None, [256], [0, 256])

#### Plot the histogram
plt.plot(hist)
plt.xlabel('Pixel Value')
plt.ylabel('Frequency')
plt.title('Histogram of Grayscale Image')
plt.show()

```

# Write the code to perform histogram equalization of the image. 
```

import cv2
import numpy as np
import matplotlib.pyplot as plt

#### Load a grayscale image
image_path = 't.jpg'
gray_image = cv2.imread(image_path, cv2.IMREAD_GRAYSCALE)

#### Perform histogram equalization
equalized_image = cv2.equalizeHist(gray_image)

#### Calculate histograms before and after equalization
hist_before = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
hist_after = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])

#### Plot the histograms
plt.figure(figsize=(10, 6))

plt.subplot(2, 1, 1)
plt.plot(hist_before)
plt.title('Original Histogram')
plt.xlabel('Pixel Value')
plt.ylabel('Frequency')

plt.subplot(2, 1, 2)
plt.plot(hist_after)
plt.title('Equalized Histogram')
plt.xlabel('Pixel Value')
plt.ylabel('Frequency')

plt.tight_layout()
plt.show()

#### Display the original and equalized images
cv2.imshow('Original Grayscale Image', gray_image)
cv2.imshow('Equalized Grayscale Image', equalized_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image
<br>![t](https://github.com/Jeswanth21001768/HISTOGRAM/assets/94155480/36213fc6-137d-43db-a488-92dca7ab4aed)
<br>

<br>![m](https://github.com/Jeswanth21001768/HISTOGRAM/assets/94155480/2f2e65b3-ae40-4f9d-b4bb-9eee54d6089e)

<br><img width="611" alt="image" src="https://github.com/Jeswanth21001768/HISTOGRAM/assets/94155480/5131b177-929c-472b-9287-64ee51bb7033">
<br><img width="583" alt="image" src="https://github.com/Jeswanth21001768/HISTOGRAM/assets/94155480/d6ce934c-4830-4c56-b0ae-30c84aba9744">



### Histogram of Grayscale Image and any channel of Color Image
<br><img width="456" alt="image" src="https://github.com/Jeswanth21001768/HISTOGRAM/assets/94155480/fd6f6cca-80d9-4e91-ae19-c641c2fb0ccf">

<br><img width="480" alt="image" src="https://github.com/Jeswanth21001768/HISTOGRAM/assets/94155480/7dd8f72e-7bcb-4576-930c-0ec1658a9c17">

<br>
<br>

### Histogram Equalization of Grayscale Image
<br><img width="940" alt="image" src="https://github.com/Jeswanth21001768/HISTOGRAM/assets/94155480/5d0f3429-18bd-4c33-87af-2a88040abe6f">
<br>
<br>
<br>

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
