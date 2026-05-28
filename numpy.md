# NumPy for OpenCV

## What is NumPy?

NumPy (Numerical Python) is a Python library used for:

- Working with arrays and matrices
- Performing mathematical operations quickly
- Storing and processing image pixel values
- Handling large amounts of numerical data efficiently

In OpenCV, images are represented as NumPy arrays.

---

# Why NumPy is Important for OpenCV

OpenCV uses NumPy because:

- Images are stored as arrays
- Pixels can be accessed using array indexing
- Image manipulation becomes easier
- Mathematical operations become faster
- Supports image processing operations

Without NumPy:

- Accessing pixels becomes difficult
- Image calculations become slow
- Many OpenCV functions cannot work properly

---

# Understanding Arrays

A NumPy array stores multiple values together.

Example of 1D Array:

```python
[10,20,30,40]
```

Example of 2D Array:

```python
[
 [1,2,3],
 [4,5,6]
]
```

Images are generally stored as 2D or 3D arrays.

---

# Import NumPy

```python
import numpy as np
```

`np` is used as a shortcut name.

---

# Creating Arrays

```python
import numpy as np

arr=np.array([1,2,3,4])

print(arr)
```

Output:

```python
[1 2 3 4]
```

---

# Create Matrix (2D Array)

```python
import numpy as np

matrix=np.array([
[1,2,3],
[4,5,6]
])

print(matrix)
```

Output:

```python
[[1 2 3]
 [4 5 6]]
```

---

# Shape of Array

Shape tells dimensions.

```python
arr=np.array([
[1,2,3],
[4,5,6]
])

print(arr.shape)
```

Output:

```python
(2,3)
```

Means:

- 2 Rows
- 3 Columns

This is useful because image size is also stored as shape.

---

# Creating Arrays Filled with Zeros

```python
img=np.zeros((300,300))
```

Creates:

- 300 Rows
- 300 Columns
- All values = 0

Useful for creating blank images.

---

# Creating White Images

```python
img=np.ones((300,300))*255
```

Creates white image because:

- 255 = White pixel value

---

# Accessing Elements

```python
arr=np.array([10,20,30])

print(arr[0])
```

Output:

```python
10
```

Images use the same concept for pixels.

---

# Accessing Pixel Values

```python
pixel=image[100,50]
```

Means:

- Row = 100
- Column = 50

Returns pixel value.

---

# Changing Pixel Values

```python
image[100,50]=255
```

Changes pixel value.

OpenCV uses this for drawing and editing images.

---

# RGB Image Structure

Color images contain 3 channels:

- Blue
- Green
- Red

Stored like:

```python
image[row,column,channel]
```

Example:

```python
blue=image[50,60,0]

green=image[50,60,1]

red=image[50,60,2]
```

---

# Array Slicing

Used to crop images.

```python
crop=image[100:200,50:150]
```

Means:

- Rows 100 to 200
- Columns 50 to 150

Creates cropped image.

---

# Mathematical Operations

Increase brightness:

```python
bright=image+50
```

Decrease brightness:

```python
dark=image-50
```

NumPy makes these operations fast.

---

# Important NumPy Functions Used in OpenCV

## np.array()

Creates arrays

## np.zeros()

Creates black images

## np.ones()

Creates white images

## np.shape

Gets image dimensions

## np.copy()

Creates copy of image

## np.reshape()

Changes dimensions

## np.mean()

Calculates average pixel intensity

## np.max()

Maximum pixel value

## np.min()

Minimum pixel value

---

# How OpenCV Uses NumPy

Image Loading:

```python
img=cv2.imread("image.jpg")
```

Actually:

- OpenCV reads image
- Converts image into NumPy array
- Stores pixel values inside array

Flow:

Image

↓

Pixel Values

↓

NumPy Array

↓

OpenCV Processing

↓

Output Image

---

# Simple Summary

NumPy helps OpenCV by:

- Storing images as arrays
- Accessing pixel values
- Modifying images
- Performing calculations
- Cropping images
- Speeding up image processing

NumPy acts like the storage and calculation engine while OpenCV acts like the toolbox used to process images.
