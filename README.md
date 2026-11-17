# edge-detection-opencv

## Aim

To perform edge detection using Sobel, Roberts, Prewitt, Laplacian, and Canny edge detectors.

---

## Software Required

- Anaconda – Python 3.7  
- Jupyter Notebook / VS Code  
- OpenCV (cv2)  
- NumPy  
- Matplotlib  

---

## ⚙️ Algorithm

### Step 1:
Import all the necessary modules for the program.

### Step 2:
Load an image using `cv2.imread()`.

### Step 3:
Convert the image to grayscale.

### Step 4:
Apply **Sobel operator** using OpenCV to detect edges.

### Step 5:
Apply **Prewitt operator** using custom kernels.

### Step 6:
Apply **Roberts operator** using custom kernels.

### Step 7:
Apply **Laplacian operator** using OpenCV.

### Step 8:
Apply **Canny edge detector** using OpenCV.

### Step 9:
Display all edge-detected images for comparison.

---

## Developed By

- **Name:** SURYA D
- **Register No:** 212224220115

---

## Output

###  Sobel Edge Detector
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('SAISHU.jpg') 
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```


###  Laplacian Edge Detector
```
Canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
```

###  Canny Edge Detector
```
image = cv2.imread("SAISHU.jpg")

gray = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
prewitt_x = np.array([[1, 0, -1],
                      [1, 0, -1],
                      [1, 0, -1]])

prewitt_y = np.array([[1, 1, 1],
                      [0, 0, 0],
                      [-1, -1, -1]])

prewitt_x_edge = cv2.filter2D(gray, -1, prewitt_x)
prewitt_y_edge = cv2.filter2D(gray, -1, prewitt_y)
prewitt = cv2.magnitude(prewitt_x_edge.astype(np.float32),
                        prewitt_y_edge.astype(np.float32))

plt.imshow(canny_edges, cmap='gray')
plt.title('Prewitt Edge Detection')
plt.axis('off')
```

## output

<img width="291" height="373" alt="image" src="https://github.com/user-attachments/assets/ab803df7-c7de-4f41-bd94-e82fd8392786" />
<br>
<img width="295" height="389" alt="image" src="https://github.com/user-attachments/assets/979d72a8-26f8-4922-8928-de516102de83" />
<br>
<img width="296" height="385" alt="image" src="https://github.com/user-attachments/assets/cbe77ae2-bee0-4556-afbb-8a25f7cad368" />
<br>
<img width="288" height="386" alt="image" src="https://github.com/user-attachments/assets/7165fc8b-3734-45e0-9178-79fcd366209f" />


## Result

Thus, edges are successfully detected using Sobel, Prewitt, Roberts, Laplacian, and Canny edge detection techniques. Each method highlights edges differently based on gradient and intensity variations, improving feature extraction and analysis.
