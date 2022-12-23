# MouseControlWithHandGesture
Libraries Used here :-
             1) Open CV
             2) MediaPipe
             3) NumPy 
             4) AutoPy

HandLandmarks(Function)
In this function we have taken the handLand marks using media pipe . here we've created an object for processing the video input and one for storing the handmarks of the object.  
after this we traverse in a loop to store the detected handmarks coordinates in a list . Here We Draws each individual index on the hand with 
connections then we have Converted the decimal coordinates relative to the image for each index and in last it appends the coordinates in the list .
After the whole Loop is traversed it returns the list containing all the co-ordinates of the handMarks of the object . 

Fingers (Function)

In this , the function is called to check which number is up here we have taken the list returned in handLandmarks function.  there are basically 3 parts of this function one it checks that if the thumb is up or not or if the tip of the finger is only up or no or 3rd if two fingers are up or not . and returns the list containing the results . where 1 being true and 0 being false .

Main code 

here first we reads the frames , changes the format to BGR to RGB and then calls the fucntion handLandmarks and stores it in imlist . then we call the fingers function to check which finger is up basically and then perform the following actions :-
1) if  the tip of the index finger is up then it will act as if to move the pointer . 
2) if the thumb is up then it will act as a leftclick
here we've used  "autopy.mouse.move(wScr - cX,cY) " this function is used to move the mouse to the x and y coordinate values values (wSrc inverts the direction)
