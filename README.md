# CV_MIdterm-Jeff


Name: Jeff Lin

Prompt 1
The task involved creating an object detection pipeline that detects blue armor plates and displays bounding boxes and depth on a live video feed using OpenCV.


We created a ColorDetection class to determine if the given frame contains mroe blue than red. Then the frame is converted to HSV. The HSV sliders were used to optimize the upper and lower of red and blue respectively. Then the findCountours() function is called when using the masks on the frames. This area is then calculared and compared, and if the blue is greater then it is a blue armor plate.


A Capture class was created to handle the video capture and frame processing. The Capture class contains a ColorDetection object The Capture class is initialized with a video source. The video source can be a camera or a video file. The Capture class contains a process_frame() method that runs the object detection pipeline on each frame. Bounding boxes are drawn around the detected blue armor plates and the confidence score is displayed. (Depth estimation is not implemented yet.)

Then a capture class was made for the handling of video capture and frame processing. This Capture class contains a ColorDetecion Object called //// 

Prompt 2
The task involved displaying the horizontal and vertical angle offset from the center of a detection. The camera resolution/FOV was used for the x and y axis to determine the respective offsets.

Design Decisions
Prompt 3 (SystemD)
The task involved creating a SystemD service daemon that runs the object detection pipeline on boot. The service file loads PyTorch, required CV libraries, and runs the object detection pipeline inside a virtual environment. The torch version is printed to the system log.

Design Decisions
Followed the instructions on the Google Slides presentation about SystemD. The service file is located in the systemd/ directory. The service file loads the virtual environment and runs the object detection pipeline. The service file is copied to /etc/systemd/system/ and the service is enabled and started. The service is started on boot.
