# Python Basics Needed for OpenCV and Image Processing

Before learning OpenCV, you should know some important Python basics.  
These concepts help you understand how images are processed inside the computer.

---

# Variables

Variables store data.

```python
name = "OpenCV"
number = 10
```

Used for:
- Image paths
- Pixel values
- Width and height values

Example:

```python
width = 640
height = 480
```

---

# Data Types

Important data types:

| Type | Example | Use |
|------|---------|------|
| int | 255 | Pixel value |
| float | 0.5 | Scaling |
| string | "image.jpg" | File name |
| boolean | True | Conditions |

Example:

```python
image_name = "cat.jpg"
pixel = 255
```

---

# Print Function

Used to display output.

```python
print("Hello")
```

Useful for:
- Debugging
- Checking image information

Example:

```python
print(image.shape)
```

---

# Operators

Math operators are important in image processing.

```python
a = 10 + 5
b = 20 - 3
c = 2 * 5
```

Used for:
- Brightness control
- Pixel calculations

---

# Conditional Statements

Used for decision making.

```python
if pixel > 200:
    print("Bright Pixel")
```

Useful for:
- Thresholding
- Object detection
- Color checking

---

# Loops

Loops repeat tasks.

## For Loop

```python
for i in range(5):
    print(i)
```

## While Loop

```python
while True:
    print("Camera Running")
```

Used for:
- Reading video frames
- Processing pixels
- Webcam capture

---

# Functions

Functions help reuse code.

```python
def greet():
    print("Hello")
```

Example:

```python
def resize_image(img):
    return cv2.resize(img, (300,300))
```

Used for:
- Image processing
- Detection systems
- Filters

---

# Lists

Lists store multiple values.

```python
colors = ["red", "green", "blue"]
```

Used for:
- Coordinates
- Multiple images
- Color values

---

# NumPy Arrays

Very important for OpenCV.

```python
import numpy as np
```

Example:

```python
arr = np.array([1,2,3])
```

In OpenCV:
- Images are stored as NumPy arrays
- Pixels are array values

---

# Indexing

Accessing array values.

```python
arr[0]
```

For images:

```python
image[100,200]
```

Means:
- Row = 100
- Column = 200

---

# Nested Loops

Used to access every pixel.

```python
for y in range(height):
    for x in range(width):
        print(x, y)
```

Used for:
- Pixel manipulation
- Image filtering
- Custom image effects

---

# File Handling

Reading and saving files.

```python
file = open("data.txt")
```

In OpenCV:

```python
cv2.imread("image.jpg")
cv2.imwrite("new.jpg", image)
```

---

# Exception Handling

Prevents program crash.

```python
try:
    print("Run")
except:
    print("Error")
```

Useful when:
- Image not found
- Camera not connected

---

# Important Libraries

| Library | Purpose |
|---------|----------|
| OpenCV | Image processing |
| NumPy | Array operations |
| Matplotlib | Image display |
| Pillow | Image editing |
| TensorFlow | AI projects |

---

# Important Concepts for Image Processing

You should know:

- Pixel
- Resolution
- RGB and BGR colors
- Grayscale image
- Binary image
- Frames in video
- FPS (Frames Per Second)

---

# Important OpenCV Functions

```python
cv2.imread()
cv2.imshow()
cv2.waitKey()
cv2.destroyAllWindows()
cv2.VideoCapture()
cv2.cvtColor()
cv2.resize()
cv2.GaussianBlur()
```

---

# Basic Image Processing Techniques

Learn these concepts:

- Image resizing
- Cropping
- Blurring
- Thresholding
- Edge detection
- Contour detection
- Object detection

---

# Simple Workflow of Image Processing

```text
Image Input
     ↓
Convert into Pixels
     ↓
Process Pixel Values
     ↓
Display Result
```

Example:
- Face detection
- Color detection
- Motion detection
- QR code scanner

---

# Final Understanding

OpenCV works mainly with:
- Pixels
- Arrays
- Mathematical operations

Every image processing project finally depends on:
- Understanding pixels
- Processing arrays
- Manipulating image data
