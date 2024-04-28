# RescuzeMaze_With_HuMoments

--------------------About The Code--------------------
This Python script integrates color and letter detection functionalities using OpenCV (Open Source Computer Vision Library) and communication with an Arduino device via serial connection. Here's a brief overview of its key components and functionalities:

Color Detection:
    The script captures video frames from a webcam and converts them to the HSV (Hue, Saturation, Value) color space.
    It defines color ranges for green, red, and yellow in the HSV format and creates masks for each color.
    Contours are then detected in each color mask to identify the presence of the respective colors in the frame.
    The detect_color() function returns a single-character representation ('R' for red, 'Y' for yellow, 'G' for green) of the detected color.

Letter Detection:
    Video frames are converted to grayscale, and a threshold is applied to segment black objects.
    Contours representing the shapes of black objects are detected in the binary image.
    Hu Moments, a set of seven mathematical descriptors of the shape of a region, are calculated for each contour.
    These moments are compared to a reference set (reference_hu_moments) to determine if a letter shape is present in the frame.
    If a letter shape is detected, the detect_letter() function returns "Letter".

Integration with Arduino:
    The script establishes a serial connection with an Arduino device.
    It continuously reads characters from the Arduino, expecting a 'L' character as a trigger to start the detection process.
    Upon receiving 'L', it performs color and letter detection on the current video frame.
    Detected color and letter information is sent back to the Arduino for further processing.

User Interface:
    The script displays the video frames with detected contours in a window titled "Colors and Letters".
    The user can exit the program by pressing the 'q' key.
    This script can serve as a foundation for various applications such as object recognition, automated sorting systems, or interactive installations where real-time color and shape detection are required, coupled with interaction with external hardware like Arduino.

--------------------Why I Make This Code?--------------------
I created this code for participation in the "Rescuze Maze 2023" competition. The competition likely required autonomous robots to navigate through a maze, identify specific objects based on color and shape, and possibly interact with them. Here's why I chose to develop this code:

Color and Shape Recognition: 
    In the maze, there might be objects of interest distinguished by their colors or shapes. Detecting these features allows the robot to identify and interact with them effectively.
    Real-Time Processing: The code is designed to process video frames from a webcam in real-time, enabling the robot to make quick decisions and navigate efficiently through the maze without delays.

Integration with Arduino: 
    By establishing communication with an Arduino device, the code enables interaction between the robot's processing unit and external hardware. This could be crucial for controlling actuators, motors, or other components of the robot based on the detected information.

Versatility: 
    The code's modular design allows for easy adaptation to different scenarios within the maze. Whether it's detecting colored markers, identifying specific shapes, or navigating based on visual cues, the code provides a versatile framework.

Competitive Advantage: 
    Participating in the "Rescuze Maze 2023" competition requires a competitive edge. By developing this code, I aimed to equip our team's robot with advanced sensing and decision-making capabilities, enhancing its chances of success in the competition.
    
By creating this code, I aimed to contribute to our team's efforts in designing a capable and intelligent robot for the "Rescuze Maze 2023" competition, ultimately striving for excellence and success in the event.
