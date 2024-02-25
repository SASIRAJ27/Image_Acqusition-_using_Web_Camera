# Image_Acqusition-_using_Web_Camera
## Aim
 
Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
Use cv2.VideoCapture(0) to access web camera
<br>

### Step 2:
Use cv2.imread to read the video or image
<br>

### Step 3:
Use cv2.imwrite to save the image
<br>

### Step 4:
Use cv2.imshow to show the video
<br>

### Step 5:
End the program and close the output video window by pressing 'q'.
<br>


## Program:
``` Python
### Developed By: SASIRAJKUMAR T J
### Register No:212222230137
```
## i) Write the frame as JPG file
```Python
import cv2
viedoCaptureObject=cv2.VideoCapture(0)
while(True):
    ret,frame=viedoCaptureObject.read()
    cv2.imwrite("PIC.JPEG",frame)
    result=False
viedoCaptureObject.release()
cv2.destroyAllWindows()
```



## ii) Display the video
```Python
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    cv2.imshow('SASIRAJKUMAR T J',frame)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```

## iii) Display the video by resizing the window
```import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=smaller_frame
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=smaller_frame
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('212222230137-SASIRAJKUMAR TJ',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```




## iv) Rotate and display the video
```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('212222230137-SASIRAJKUMAR TJ',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## Output

### i) Write the frame as JPG image
![Screenshot 2024-02-25 091141](https://github.com/SASIRAJ27/Image_Acqusition-_using_Web_Camera/assets/113497176/62b8582c-93d9-475c-9fed-02e30195d449)



### ii) Display the video

![PIC](https://github.com/SASIRAJ27/Image_Acqusition-_using_Web_Camera/assets/113497176/78ab7ed7-a000-49c6-80bb-6d996caeaa29)



### iii) Display the video by resizing the window

![Screenshot 2024-02-25 091321](https://github.com/SASIRAJ27/Image_Acqusition-_using_Web_Camera/assets/113497176/7678122f-882c-45ea-8ee5-66ff55d8be42)




### iv) Rotate and display the video

![Screenshot 2024-02-25 091603](https://github.com/SASIRAJ27/Image_Acqusition-_using_Web_Camera/assets/113497176/8aca415b-cd4e-47bc-8628-e640f90fe81b)






## Result:
Thus the image is accessed from webcamera and displayed using openCV.
