# dip_project
In this project, we aim to develop a real-time face detection system using MATLAB. The code utilizes the vision.CascadeObjectDetector object to detect faces within a live video stream captured from a webcam. Additionally, we employ the vision.VideoPlayer object to display the video feed with annotated bounding boxes around detected faces.

The key components of the code include:

Face Detector Initialization: We create a vision.CascadeObjectDetector object named faceDetector. This object is trained to detect faces based on a predefined cascade classifier.
Webcam Initialization: A webcam object (cam) is created to capture live video frames. This allows us to process real-time data for face detection.
Video Player Initialization: The vision.VideoPlayer object (videoPlayer) is set up to display the video feed with annotated bounding boxes around detected faces. This provides a visual representation of the face detection process.
Main Loop: Within a while loop, the code continuously captures video frames from the webcam (snapshot(cam)), converts them to grayscale (rgb2gray(videoFrame)), and detects faces using the faceDetector object (bbox = step(faceDetector, videoFrameGray)).
Face Annotation: Bounding boxes are drawn around detected faces using insertShape to visually indicate the regions where faces are detected.
Real-Time Display: The annotated video frames are displayed in real-time using the videoPlayer object (step(videoPlayer, videoFrame)).
Loop Termination: The while loop continues until a specified number of frames (frameCount < 400) or until the video player window is closed (isOpen(videoPlayer)).
