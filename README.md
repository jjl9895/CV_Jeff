# CV_MIdterm-Jeff


Name: Jeff Lin

Prompt 1

We created a ColorDetection class to determine if the given frame contains mroe blue than red. Then the frame is converted to HSV. The HSV sliders were used to optimize the upper and lower of red and blue respectively. Then the findCountours() function is called when using the masks on the frames. This area is then calculared and compared, and if the blue is greater then it is a blue armor plate. The confidence threshold is 0.25. 


Then a Capture class was made for the handling of video capture and frame processing. This Capture class contains a ColorDetecion object. Then we also have a video source that is in the __init__. This video source is could be a video file or a camera. The Capture class also contains a process_fram() method. This method runs an object detection pipeline on each frame and the bounding boxes are then created when detecting blue armor plates. The confidence scroe is also displayed along with the box.  

Prompt 2

We used the bounding box coordinates to process the needed angle offsets so that the gimble could aim properly. The get_coordinates function gets the coordinates of the frame and returns (x_min, y_min, x_max, y_max) or returns none if the length of "rows" is 0. Then tis get_coordinates method is called later to find the median depth from the depth frame. 


Prompt 3

SystemD was created with the tutorial on Google Slides. This included a service file aswell. The service file will load the virtual environment and run the object detection pipeline automatically on start. The service file is copied to /etc/systemd/system/.



