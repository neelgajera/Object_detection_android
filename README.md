# Object_detection_android

In App Create 2 Main Activity 
-Camara Activity Which Load Camara Stream And Data TO detection Activity
 ->> CameraActivity.java
-  Detector Activity Which Process Data Stream And Process Output
 ->> DetectorActivity.java
  * algo
    - Intalize Yolo5Detection.class and load model From Assets (YoloV5Classifier.java)
    - Then Detarmin Input And Privew size (and make Transformation Matrix which can convert input stream bitmap to model input size (640,640)
    - and also convert Inverse martix which can invers process for output show
    - Converted Results Class pass to another tracking activity (MultiBoxTracker.java)
    - and also some other function which can change (cpu/gpu/nnapi)
  
- customview/
  View's class for displaying results to ui
  
- env/
  - class related to image data converter funcutions
  - loading from assets functions
  - logger

- tflite/
  - object detector class ,which laod model from assets and process image 
  - YoloV5Classifier.java -> YoloV5Classifier.recognizeImage (take (640,640) bitmap image -> recognize class list for that dimantion )
  
- tracking/
  - which can track output from detector activity and pass them to ui 
  
