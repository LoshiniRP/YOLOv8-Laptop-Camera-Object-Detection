# YOLOv8 Object Detection Using Laptop Camera

## Aim

To access the **laptop camera**, capture an image, and detect objects using **YOLOv8**.

## Requirements

* Anaconda
* Jupyter Notebook
* Laptop Camera

## Steps

1. Open **Jupyter Notebook** using Anaconda.
2. Access your **laptop camera** using OpenCV.
3. Wait for **5 seconds** and capture an image.
4. Display the captured image.
5. Apply **YOLOv8 object detection**.
6. Display the detected image with **bounding boxes and labels**.

## Algorithm

```text
Laptop Camera
      ↓
Capture Image
      ↓
Display Image
      ↓
YOLOv8 Detection
      ↓
Display Detected Objects
```


## GitHub Reference
https://github.com/ultralytics/ultralytics
**Platform:** Anaconda + Jupyter Notebook only.

## Program:
Name: R P Loshini
Register Number: 212225230155

```
# Object Detection Using Web Camera
# YOLOv8 + OpenCV

# Install once in Jupyter/Command Prompt:
# pip install ultralytics opencv-python
import cv2
from ultralytics import YOLO

# Load a pretrained YOLOv8 model
model = YOLO("yolov8n.pt")

# Open the default webcam
cap = cv2.VideoCapture(0)
if not cap.isOpened():
 print("Error: Cannot open webcam.")
 raise SystemExit
while True:
 ret, frame = cap.read()
 if not ret:
 print("Error: Cannot read webcam frame.")
 break

 # Run object detection
 results = model(frame, verbose=False)

 # Draw bounding boxes, class names and confidence
 annotated_frame = results[0].plot()
 cv2.imshow("Object Detection - Web Camera", annotated_frame)

 # Press q to quit
 if cv2.waitKey(1) & 0xFF == ord("q"):
 break

cap.release()
cv2.destroyAllWindows()
```

## Output:
<img width="416" height="672" alt="image" src="https://github.com/user-attachments/assets/bdd4f3f6-f4ea-4cc7-b3af-c655c935016b" />

## Result:
Thus, YOLOv8 Object Detection Using Laptop Camera has been executed successfully.
