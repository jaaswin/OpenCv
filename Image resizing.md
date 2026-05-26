# Image Resizing in OpenCV

Image resizing means changing the **width** and **height** of an image.

It is like stretching, shrinking, or fitting a photo into a new frame.

---

# Why Image Resizing is Important

Images from cameras can be very large.

Example:
- 4000 × 3000 pixels

Large images:
- Use more memory
- Slow down processing
- Reduce real-time performance

So we resize images to:
- Make processing faster
- Match screen size
- Prepare images for AI models
- Reduce storage space

---

# Understanding Image Size

Image size is written as:

```text
Width × Height
```

Example:

```text
1920 × 1080
```

- Width → horizontal pixels
- Height → vertical pixels

More pixels = more image detail.

---

# What Happens During Resizing

When resizing:
- OpenCV creates a new image size
- Pixel values are recalculated

Example:

Original:
```text
1000 × 1000
```

Resize to:
```text
500 × 500
```

The image becomes smaller.

---

# Types of Resizing

## Shrinking

Reduce image size.

Example:

```text
1920×1080 → 640×480
```

Benefits:
- Faster processing
- Less memory usage

---

## Enlarging

Increase image size.

Example:

```text
300×300 → 1200×1200
```

Problem:
- Image may become blurry
- Pixels get stretched

Like zooming too much into a photo.

---

# Resizing in OpenCV

OpenCV uses:

```python
cv2.resize()
```

Basic syntax:

```python
resized = cv2.resize(image, (width, height))
```

---

# Example Program

```python
import cv2

# Read image
img = cv2.imread("photo.jpg")

# Resize image
resized = cv2.resize(img, (500, 400))

# Show image
cv2.imshow("Resized Image", resized)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

---

# Maintaining Aspect Ratio

Aspect ratio means:
- Relationship between width and height

Example:

```text
16:9
```

If aspect ratio changes:
- Image may look stretched
- Circle may become oval

Correct:

```text
800×600 → 400×300
```

Incorrect:

```text
800×600 → 400×100
```

---

# Resize Using Scale Factors

Instead of exact size, we can scale image.

Example:
- Half size
- Double size

```python
resized = cv2.resize(img, None, fx=0.5, fy=0.5)
```

Here:
- `fx` → width scale
- `fy` → height scale

`0.5` means half size.

---

# Interpolation in Resizing

Interpolation decides:
- How new pixels are calculated

Important methods:

## INTER_AREA

Best for shrinking images.

```python
cv2.INTER_AREA
```

---

## INTER_LINEAR

Default method.
Good for normal resizing.

```python
cv2.INTER_LINEAR
```

---

## INTER_CUBIC

Better quality for enlarging.
But slower.

```python
cv2.INTER_CUBIC
```

---

# Example with Interpolation

```python
resized = cv2.resize(
    img,
    (800, 600),
    interpolation=cv2.INTER_CUBIC
)
```

---

# Real Applications of Image Resizing

## Face Detection
Resize frames for faster detection.

---

## AI Models
Neural networks need fixed image size.

Example:

```text
224×224
416×416
640×640
```

---

## Video Streaming
Reduce resolution for smooth streaming.

---

## Mobile Apps
Smaller images reduce memory usage.

---

# Important Note

Very small resizing:
- Loses details

Very large resizing:
- Causes blur

Good resizing keeps balance between:
- Speed
- Quality
- Memory

---

# Simple Analogy

Imagine drawing a picture on graph paper.

- Smaller graph → less detail
- Larger graph → stretched picture

Image resizing works similarly with pixels.
