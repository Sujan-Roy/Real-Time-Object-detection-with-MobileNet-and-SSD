# Real-Time-Object-detection-with-MobileNet-and-SSD
Real-time object detection with MobileNet and SSD is a process of detecting objects in real time using the MobileNet and SSD object detection models. MobileNet is a lightweight, fast, and accurate object detection model that can be used on mobile devices. SSD is a single-shot object detection model that can detect objects in real time.

To perform real-time object detection with MobileNet and SSD, you will need the following:

1. A computer or mobile device with a webcam or video input
2. The MobileNet and SSD object detection models
3. An object detection library, such as OpenCV or TensorFlow

Once you have all of the required components, you can follow these steps to perform real-time object detection:

1. Install the object detection library on your computer or mobile device.
2. Load the MobileNet and SSD object detection models into the object detection library.
3. Start the webcam or video input.
4. Loop over the frames of the webcam or video input.
5. For each frame, detect objects using the MobileNet and SSD object detection models.
6. Draw the bounding boxes around the detected objects.
7. Display the frames with the detected objects.

# Requirements
Make sure you have the following files in the same directory as the Python script:

1. MobileNetSSD.txt (the Caffe model architecture file)
2. MobileNetSSD_deploy.caffemodel (the pre-trained model weights file)

The code captures frames from the webcam, performs object detection using the MobileNet SSD model, and displays the resulting frames with bounding boxes and class labels. Press 'q' to quit the application.

# Error
```sh
1.  
[libprotobuf ERROR C:\projects\opencv-python\opencv\3rdparty\protobuf\src\google\protobuf\text_format.cc:288] Error parsing text-format opencv_caffe.NetParameter: 2:1: Invalid control characters encountered in text.
[libprotobuf ERROR C:\projects\opencv-python\opencv\3rdparty\protobuf\src\google\protobuf\text_format.cc:288] Error parsing text-format opencv_caffe.NetParameter: 2:2: Interpreting non ascii codepoint 162.
[libprotobuf ERROR C:\projects\opencv-python\opencv\3rdparty\protobuf\src\google\protobuf\text_format.cc:288] Error parsing text-format opencv_caffe.NetParameter: 2:2: Expected identifier, got: ?
Traceback (most recent call last):
  File "src/facedetect/main.py", line 54, in <module>
    util.gainFaceByDNN(path, modelpath, deploypath)
  File "src/facedetect/detector.py", line 26, in gainFaceByDNN
    net = cv2.dnn.readNetFromCaffe(modelFile, configFile)
cv2.error: OpenCV(4.0.0) C:\projects\opencv-python\opencv\modules\dnn\src\caffe\caffe_io.cpp:1151: error: (-2:Unspecified error) FAILED: ReadProtoFromTextFile(param_file, param). Failed to parse NetParameter file: D:\project\python\IQA\src\facedetect\res10_300x300_ssd_iter_140000.caffemodel in function 'cv::dnn::ReadNetParamsFromTextFileOrDie'

2. 
detector = cv2.dnn.readNetFromCaffe(protoPath, modelPath)

error: OpenCV(4.1.2) C:\projects\opencv-python\opencv\modules\dnn\src\caffe\caffe_io.cpp:1121: error: (-2:Unspecified error) FAILED: fs.is_open(). Can't open "C:\Users\osama\Desktop\opencv-face-recognitio\face_detection_model\deploy.prototxt.txt" in function 'cv::dnn::ReadProtoFromTextFile
```

# Error Solve
To resolve the two aforementioned issues, you can follow these steps:

1. Delete the existing "MobileNetSSD.txt" file from the directory.

2. Create a new "MobileNetSSD.txt" file in the same directory.

3. Download the "MobileNetSSD.txt" file from the provided link.

https://github.com/chuanqi305/MobileNet-SSD/blob/master/voc/MobileNetSSD_deploy.prototxt

# Runnning this file
Use the below commond to execute the python file:- 
```sh
python main.py --prototxt MobileNetSSD.txt --model MobileNetSSD_deploy.caffemodel
```
