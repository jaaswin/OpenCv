# Meaning of 0, 1, and -1 in OpenCV While Opening Images

When using:

```python
cv2.imread()
```

the second parameter tells OpenCV **how to read the image**.

Syntax:

```python
img = cv2.imread("image.jpg", value)
```

Here, `value` can be:

- 0
- 1
- -1

---

# 1 → Read Image as Color Image (Default)

```python
img = cv2.imread("image.jpg",1)
```

or simply:

```python
img = cv2.imread("image.jpg")
```

Meaning:

- Loads image as color image
- OpenCV reads image in BGR format
- Creates 3 channels

Output shape:

```python
(height,width,3)
```

Example:

```python
img=cv2.imread("cat.jpg",1)

print(img.shape)
```

Output:

```python
(480,640,3)
```

Means:

- Height = 480

- Width = 640

- 3 Color Channels

---

# 0 → Read Image as Grayscale

```python
img=cv2.imread("image.jpg",0)
```

Meaning:

- Converts image into grayscale
- Only one channel is stored
- Faster processing

Output shape:

```python
(height,width)
```

Example:

```python
img=cv2.imread("cat.jpg",0)

print(img.shape)
```

Output:

```python
(480,640)
```

Only rows and columns.

---

# -1 → Read Original Image Without Modification

```python
img=cv2.imread("image.png",-1)
```

Meaning:

- Reads image exactly as stored
- Keeps transparency channel
- Does not remove extra channels

Example:

Suppose PNG contains:

```text
Blue
Green
Red
Alpha (Transparency)
```

Using:

```python
img=cv2.imread("logo.png",-1)
```

Output shape:

```python
(height,width,4)
```

Because:

```text
B G R A

4 Channels
```

---

# Quick Comparison

| Value | Meaning | Channels |
|------|------|------|
| 1 | Color Image | 3 |
| 0 | Grayscale | 1 |
| -1 | Original Image | Depends |

---

# Example Program

```python
import cv2

color=cv2.imread("image.jpg",1)

gray=cv2.imread("image.jpg",0)

original=cv2.imread("image.png",-1)

cv2.imshow("Color",color)

cv2.imshow("Gray",gray)

cv2.imshow("Original",original)

cv2.waitKey(0)

cv2.destroyAllWindows()
```

---

# Simple Understanding

```text
1

↓

Read Color Image


0

↓

Read Black and White (Grayscale)


-1

↓

Read Image Exactly As It Is Stored
```
