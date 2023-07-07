# VirtualCalc

This project is a simple calculator program that utilizes hand tracking and gestures to perform arithmetic calculations. It uses the OpenCV library and the HandTrackingModule from the cvzone library to detect hand movements and recognize button clicks.

*The program starts by initializing the webcam capture and creating an instance of the HandDetector class. It also defines a Button class that represents each calculator button. The buttons are created in a 4x4 grid and stored in a buttonList.*

The main loop of the program continuously captures frames from the webcam and performs the following steps:

#### Detect hands: 
The HandDetector is used to find hands in the frame. If a hand is detected, the landmarks of the hand are obtained.

#### Draw buttons: 
The program draws the calculator buttons on the frame using OpenCV functions. Each button is represented by a rectangle filled with a light color, with the button value displayed in the center.

#### Check for button clicks: 
The program checks if any button is clicked by comparing the hand landmarks with the button positions. If a button is clicked, its value is retrieved and added to the equation string.

#### Evaluate equation: 
If the '=' button is clicked, the program evaluates the equation using the eval() function in Python and stores the result in the myEquation variable.

#### Display equation and result: 
The program displays the current equation and the result on the frame using OpenCV's putText() function.

#### Clear equation: 
Pressing the 'c' key clears the equation.

#### Display frame: 
The program displays the processed frame with buttons, equation, and result using the cv2.imshow() function.

