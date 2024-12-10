# Camera Tracking Tutorial

You will need to know how to:
- How to create objects
- How to create C# scripts
- How to assign objects

First, create an object and a plane. in my example i will be using a cube and setting the scene up like so:
![image](https://github.com/user-attachments/assets/887580cd-fa0a-4704-b1a8-a0f462b2f711)

The cube will be our "player" and the plane exists to make it easier to itentfy the player moving around.

Next, we are going to give the player a simple movment code to make testing the camera tracking easier later on.

Create a new C# script and call it something like "Player" or "Movment", something that is easy to idenify. I will be using "Player" for my example.

You can then use the code below to allow you to use WASD or your arrow keys to move the player.
![image](https://github.com/user-attachments/assets/5f7f13b1-136f-498d-bd6b-1091647f9dea)

After doing that, make sure that the code is attached to the player object like so:

![image](https://github.com/user-attachments/assets/0029c012-76e7-4e21-bc22-8d03a23b01e0)

If it isn't, make sure to drag it into the inspector (with the player selected) or onto the object itself.

You should then make sure the code works by pressing play on the scene and testing if the cube moves.

If things are working up to this point, you should see the player object moving around, but the camera does not follow it and only sticks to one spot.
If the cube does not move, there may be an error in the way you have typed out the code.



Now, you can move onto making the camera track the cube.


Create a new C# script and name it something like "OcbjectTracking". I will be naming my C# script "Tracking" to make things simpler.

After that, open the C# script and insert these 4 lines of code inside the "public class" starting on line 7.

![image](https://github.com/user-attachments/assets/2f60f53a-58fe-4dd1-93e5-b8ff809f8729)

This creates static values that we can call upon and modify in the future.

This code below allows the camera to maintain a specific distance from the player which is usefull for simple camera tracking.
![image](https://github.com/user-attachments/assets/df0ca481-57ed-4b90-bfcb-e37216f69ab1)


The code below will call the position of our "trackedObject" (being the player object) and the "updateSpeed" for how fast the camera will move. 

Time.Delta is referenceing the frame rate in unity to figure out how fast the camera should be moving while it tracks the camera.

![image](https://github.com/user-attachments/assets/a97c34cb-32d1-4557-9269-c53885caa305)

~~"updateSpeed" gets referenced by unity every frame that unity is running. If unity is set to run at 60fps, then the camera will update it's position once every 1/60th of a second. Using "deltaTime" will check if the camera is being updated every 1/60th of a second and ties it's update speed to the framerate.~~

"transform.position" is telling the camera to move every frame and Vector3.MoveTowards allows the camera to follow the player object across the axes.

"trackedObject" is refrenceing the object that we had initially paired to our camera, which is our player object.

If you wish to, you can press play on the scene and test out the camera tracking, you should notice that the camera now tracks the player object but is too slow to keep up with it completely.

Our default speed for the camera is 3 units pers second, which we set at the beginning of the code. This can be changed outside of microsoft visual studio
Because it is set as a public value which makes changing it's tracking speed a lot easier as there isn't a need to open the script each time to change it.

in order to make sure that the camera can keep up with our player objecct, you go into the inspector for the camera and change the public value of the camera's speed from 3 to something faster like 10.

![image](https://github.com/user-attachments/assets/5f91fbb4-f577-4d88-b50a-26d94b1fbba7)



If you want your changes to the camera speed to be permanent, you can go into the code and change this value below:

![image](https://github.com/user-attachments/assets/445db202-07b1-4d9a-be80-0518e36dec3a)

that should be all for this tutorial. if you press play on your scene you should now see that the camera is trackiig the player object as it moves. 

