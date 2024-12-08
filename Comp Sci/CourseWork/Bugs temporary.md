#### Camera zoom not working - fixed
The input axis is not taking an input but it is changing the value to 0, this stops the camera from zooming at all. - fixed by using Input.mouseScrollDelta instead of Input.GetAxis
#### Camera collision 
so far - no collision or compiler errors. 

Camera View angles 
should be limited to 8 below player and 16 above, this means the camera will not break as the angle will never get too high 