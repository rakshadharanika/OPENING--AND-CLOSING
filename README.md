# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step-1
Read the Image:Load the input color image from a specified path.
### Step-2
Convert to Grayscale:Transform the color image into a grayscale format for easier processing.
### Step-3
Edge Detection:Apply an edge detection technique to identify the prominent edges in the grayscale image.
### Step-4
Create Structuring Element:Define a kernel (structuring element) for use in morphological operations, typically a matrix of ones.
### Step-6
Morphological Operations:Perform morphological operations.
Opening: Remove small objects from the edges to clean up the image.
Closing: Fill small holes in the detected edges to enhance the structure.
### Step-7
Display Results:Show the original grayscale image, along with the results of the opening and closing operations for visual comparison.

 
## Program:
```
Developed by : V RAKSHA DHARANIKA
Register Number : 212223230167
```

### Import the necessary packages
``` Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
```


### Create the Text using cv2.putText
``` Python
image = np.zeros((300, 600, 3), dtype="uint8")
text = "Keerthi vasan"
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, text, (50, 150), font, 2, (255, 255, 255), 3)
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.subplot(1, 1, 1)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")
```


### Create the structuring element
``` Python
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
```


### Use Opening operation
``` Python
opening_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
opening_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
opening_image_rgb = cv2.cvtColor(opening_image, cv2.COLOR_BGR2RGB)
plt.subplot(1, 1, 1)
plt.imshow(opening_image_rgb)
plt.title("Opening Operation")
plt.axis("off")
```



### Use Closing Operation

``` Python
closing_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
closing_image_rgb = cv2.cvtColor(closing_image, cv2.COLOR_BGR2RGB)
plt.subplot(1, 1, 1)
plt.imshow(closing_image_rgb)
plt.title("Closing Operation")
plt.axis("off")
```




## Output:

### Display the input Image
![image](https://github.com/user-attachments/assets/da740f90-2446-4e1c-b6a1-a6f032253574)





### Display the result of Opening

![image](https://github.com/user-attachments/assets/13a01c4c-854e-4e72-9bfe-374a51e6e759)



### Display the result of Closing

![image](https://github.com/user-attachments/assets/9975593c-6cd0-440c-bace-75e29ac9006f)



## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
