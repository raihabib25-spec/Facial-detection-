# Facial-detection-
pip install opencv-python
import cv2 
#load the face detection program:
face_cascade = cv2.CascadeClassifier('face_detector.xml')
#img defining in program
img = cv2.imread('image.jpg')
#Faces detection in an image
faces = face_cascade.detectMultiScale(img, 1.1, 4)
#rectangle drawing around detected faces 
for (x, y, w, h) in faces: 
  cv2.rectangle(img, (x, y), (x+w, y+h), (255, 0, 0), 2)
cv2.imwrite("face_detected.png", img) 
print('Successfully saved')
Code language: Python (python)

