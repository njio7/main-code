# Camera Tracking Tutorial

You will need to know how to
- How to create objects
- How to create C# scripts
- 
-

First, create an object and a plane. in my example i will be using a cube and setting the scene up like so:
![image](https://github.com/user-attachments/assets/887580cd-fa0a-4704-b1a8-a0f462b2f711)

The cube will be our "player" and the plane exists to make it easier to itentidy the player moving around.

Next, we are going to give the player a simple movment code to make testing the camera tracking easier later on.

Create a new C# script and call it something like "Player" or "Movment", something that is easy to idenify. I will be using "Player" for my example.

You can then use the code below to allow you to use WASD or your arrow keys to move the player.
![image](https://github.com/user-attachments/assets/5f7f13b1-136f-498d-bd6b-1091647f9dea)

After doing that, make sure that the code is attached to the player object like so:

![image](https://github.com/user-attachments/assets/0029c012-76e7-4e21-bc22-8d03a23b01e0)

If it isn't, make sure to drag it into the inspector or onto the object itself.

You should then make sure the code works by pressing play on the scene and testing if the cube moves.

If things are working up to this point, you should se the player object moving around, but the camera does not follow it and only sticks to one spot.
If the cube does not move, there may be an error in the way you have typed out the code.

Now, you can move onto making the camera track the cube.


Create a new C# script and name it something like "OcbjectTracking". I will be naming my C# script "Tracking" to make things simpler.

After that, open the C# script and insert these 4 lines of code inside the "public class" starting on line 7.

![image](https://github.com/user-attachments/assets/2f60f53a-58fe-4dd1-93e5-b8ff809f8729)

This creates static values that we can call upon and modify in the future.

This code below allows the camera to maintain a specific distance from the player which is usefull for simple camera tracking.
![image](https://github.com/user-attachments/assets/df0ca481-57ed-4b90-bfcb-e37216f69ab1)

