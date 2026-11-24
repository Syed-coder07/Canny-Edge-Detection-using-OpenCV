## Canny-Edge-Detection-using-OpenCV

## Overview :

This project demonstrates the implementation of the Canny Edge Detection algorithm using Python and OpenCV. Canny Edge Detection is a widely used image processing technique for identifying object boundaries and significant intensity changes in an image.

## License:

This project is licensed under the MIT License.

## Objectives :

* Load and process a sample image.
* Convert the image to grayscale.
* Apply the Canny Edge Detection algorithm.
* Visualize and analyze the detected edges.
* Study the impact of different threshold parameters on edge detection results.

## Technologies Used :

* Python
* OpenCV
* NumPy
* Matplotlib
* Jupyter Notebook

## Algorithm :

* Read the input image.
* Convert the image to grayscale.
* Apply Gaussian filtering to reduce noise.
* Compute image gradients.
* Perform non-maximum suppression.
* Apply double thresholding.
* Track edges using hysteresis.
* Display the detected edges.

## Applications :

* Object Detection
* Image Segmentation
* Medical Image Analysis

## Requirements :

```
pip install opencv-python numpy matplotlib
```

## Running the Project:

1. Clone the repository:

```
git clone https://github.com/your-username/canny-edge-detection-opencv.git
```

2. Open Jupyter Notebook:

```
jupyter notebook
```

3. Run:

```
CANNY EDGE DETECTION.ipynb
```

## PROGRAM :

```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread(
    r"C:\Users\syedf\OneDrive\Documents\DIPT\Syed1.png",
    cv2.IMREAD_GRAYSCALE
)

if img is None:
    print("Image not found!")
else:
    blurred = cv2.GaussianBlur(img, (5, 5), 0)
    edges = cv2.Canny(blurred, 50, 150)

    plt.figure(figsize=(10, 5))

    plt.subplot(121)
    plt.imshow(img, cmap='gray')
    plt.title('Original Image')
    plt.axis('off')

    plt.subplot(122)
    plt.imshow(edges, cmap='gray')
    plt.title('Detected Edges')
    plt.axis('off')

    plt.show()
```

## Output:

<img width="945" height="545" alt="image" src="https://github.com/user-attachments/assets/9ca755bf-006e-4ac4-887a-7d17e5bceaa4" />

## RESULT:

The Canny Edge Detection algorithm effectively detects object boundaries and important image features. The quality of edge detection depends on the selected threshold values, making parameter tuning an essential part of image processing applications.
