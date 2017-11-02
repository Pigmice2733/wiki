Vision Tracking!!! It allows the robot to see. It likes shiny tape.


OpenCV Library!! (Open Source Computer Vision Library)
It's a thing. Use it.

HSV stands for hue saturation value. Each can range from 0-255.

Start by importing numpy and cv2.

```python
import numpy as np
import cv2
```
Then get the picture.

Example:
```python
img = cv2.imread('input.jpg', 1)
```

Then set the range of color you are looking for in the image.

Example:
```python
lower_orange = np.array([0, 90, 0])
upper_orange = np.array([255, 255, 255])
```
A mask covers everything not in the range of colors specified.

Example:
```python
mask = cv2.inRange(hsv, lower_orange, upper_orange)
```



