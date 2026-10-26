## Image_Acqusition-_using_Web_Camera
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
<br>
Import OpenCV Package.

### Step 2:
<br>
Capture Video from Webcam. Use VideoCapture(0) to access the webcam and start capturing video.

### Step 3:
<br>
Read Video or Image. Utilize 'imread' to read a video frame or image from the webcam.

### Step 4:
<br>
Save Image to File. Employ 'imwrite' to save the captured image to a file.

### Step 5:
<br>
Display Video or Image. Use 'imshow' to display the captured video frame or image.

### Step 6:
<br>
End Program with 'q'. Allow the program to be terminated by pressing the 'q' key.

## Program:
### Developed By: SHARAN KUMAR G
### Register No: 212224230260
``` Python

## i) Write the frame as JPG file

import cv2
import matplotlib.pyplot as plt
from IPython.display import clear_output
import time
cap = cv2.VideoCapture(0)
ret, frame = cap.read()
if ret:
    cv2.imwrite("captured_frame.jpg", frame)
cap.release()
captured_image = cv2.imread('captured_frame.jpg')
plt.imshow(captured_image[:,:,::-1])
plt.title('Captured Frame')
plt.axis('off')
plt.show()


## ii) Display the video

cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    frame_rgb = cv2.cvtColor(frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()

## iii) Display the video by resizing the window


cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    resized_frame = cv2.resize(frame, (100, 150))  # Resize to 320x240
    frame_rgb = cv2.cvtColor(resized_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()
  
## iv) Rotate and display the video

cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    rotated_frame = cv2.rotate(frame, cv2.ROTATE_90_CLOCKWISE)
    frame_rgb = cv2.cvtColor(rotated_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release() 

```
## Output

### i) Write the frame as JPG image
</br>

<img width="642" height="512" alt="image" src="https://github.com/user-attachments/assets/a81f64fd-e67d-4697-960a-ca22ffba99d4" />


</br>


### ii) Display the video
</br>

<img width="647" height="497" alt="image" src="https://github.com/user-attachments/assets/7619101a-4a8a-4b65-93d0-296a75c44647" />


</br>


### iii) Display the video by resizing the window
</br>

<img width="340" height="491" alt="image" src="https://github.com/user-attachments/assets/590f35c2-7909-461d-855e-57db8a618914" />



</br>



### iv) Rotate and display the video
</br>

<img width="373" height="487" alt="image" src="https://github.com/user-attachments/assets/396b6d46-1c12-40ec-ae16-2df44376e922" />


</br>





## Result:
Thus the image is accessed from webcamera and displayed using openCV.
