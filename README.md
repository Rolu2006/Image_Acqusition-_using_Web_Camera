
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
<br>Use cv2.VideoCapture(0) to access web camera.


### Step 2:
<br>Use cv2.imread to read the video or image

### Step 3:
<br>Use cv2.imwrite to save the image.

### Step 4:
<br>Use cv2.imshow to show the video.


### Step 5:
<br>End the program and close the output video window by pressing 'q'.


## Program:
``` Python
### Developed By:somalaraju rohini
### Register No:212224240156

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
resized_frame = cv2.resize(frame, (100, 150)) # Resize to 320x240
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
</br>





<img width="620" height="433" alt="Screenshot 2025-10-09 102850" src="https://github.com/user-attachments/assets/77e8d30e-4d45-4829-905f-adc260c8e41c" />



### ii) Display the video
</br>
</br>




<img width="611" height="459" alt="Screenshot 2025-10-09 102953" src="https://github.com/user-attachments/assets/3ca749ca-6fbc-4ee3-b45f-5f8eab9552c2" />


### iii) Display the video by resizing the window
</br>
</br>





<img width="309" height="456" alt="Screenshot 2025-10-09 103023" src="https://github.com/user-attachments/assets/750f06dd-2523-4539-9301-e0612ddf4c4b" />


### iv) Rotate and display the video
</br>
</br>





<img width="347" height="465" alt="Screenshot 2025-10-09 103043" src="https://github.com/user-attachments/assets/534e3b49-9f9f-4eb5-bc91-087d5b7fd2dd" />



## Result:
Thus the image is accessed from webcamera and displayed using openCV.
