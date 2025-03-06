# Brick_Breaker

INTRODUCTION:
Breakout is a traditional arcade game developed and published by Atari, Inc. And Brick Breaker is a clone of Breakout   I made an interactive game based upon the classic game brick breaker. The object of brick breaker is to break the bricks that are distributed around the top of the game screen. The game consists of 48 bricks on the top of the screen, a flying ball and a movable slider on the bottom of the screen. Three unbreakable walls on the side of the screen are used to deflect the ball. Bricks are broken after coming in contact with a ball that bounces around the screen. At the bottom there is a slider that moves based on user input. The user has to make sure the ball bounces off the slider without going off the bottom of the screen. The game will continuously proceed as long as the ball is not falling out of the screen .  Once it get fell out of screen it will show “GAME OVER ”.

REQUIREMENT:
Programming Language: Java
Libraries & classes:   
1.	javax.swing.JFrame :-  An extended version of java.awt.Frame that adds support for the JFC/Swing component architecture. 
2.	java.awt.BasicStroke :- The BasicStroke class defines a basic set of rendering attributes for the outlines of graphics primitives, which are rendered with a Graphics2D object that has its Stroke attribute set to this BasicStroke.
3.	java.awt.Color :- The Color class is used to encapsulate colors in the default sRGB color space or colors in arbitrary color spaces identified by a ColorSpace
4.	java.awt.Graphics2D :- This Graphics2D class extends the Graphics class to provide more sophisticated control over geometry, coordinate transformations, color management, and text layout. This is the fundamental class for rendering 2-dimensional shapes, text and images on the Java(tm) platform.
5.	java.awt.event.* :- it provides interfaces and classes for dealing with different types of events fired by AWT components.
6.	javax.swing.* :-  Provides a set of "lightweight" (all-Java language) components that, to the maximum degree possible, work the same on all platforms.
7.	java.awt.* :- Contains all of the classes for creating user interfaces and for painting graphics and images. A user interface object such as a button or a scrollbar is called, in AWT terminology, a component. The Component class is the root of all AWT components.
8.	javax.swing.Timer :-  Fires one or more ActionEvents at specified intervals.

Software: Eclipse

IMPLEMENTATION 

1)Main.java  

a)	importing library javax.swing.Jframe for creating a Frame for window of program
b)	Setting up the dimensions of the frame and creating its object. 
c)	Calling Gameplay in mains 


2) MapGenerator.java 

1) Importing the Required Classes 
a)java.awt.BasicStroke :-  The BasicStroke class defines a basic set of rendering attributes for the outlines of graphics primitives . Here I have used this pacakage for differentiating the bricks.  
b)java.awt.Color :-   this class  is used to define the color .
c)java.awt.Graphics2D :-  This class provide more sophisticated control over geometry, coordinate transformations, color management, and text layout. I have used this class for drawing our 2D map. 

2)Creating MapGenerator class :-In this class , firstly  I have defined the 2D array for our map. 
Next is I have initialize a constructor  which will  help to generate a number of rows and columns .
Here I have add 1 to every element of array because It will detect that a particular bricks has  not intersected with ball .as its value is 1 . this will helps us to show that particular brick on screen.


3)Draw function:- Here I have created a draw function  which will draw the 2d brick map .
I have given condition that if the value of the array element is greater than 0 , i.e  equal to 1 then it will draw the brick  of white color . next to differentiate the bricks I have set a stroke of width 3 and black color here.

setBrickValue :- this function sets the value of 2D array element to 0 or 1 depending on the interaction with the ball.



3) Gameplay.java 

1)	Here I have imported all the required classes 
1.	java.awt.event.* :- it provides interfaces and classes for dealing with different types of events fired by AWT components. So for keyListener and actionListener I are going to need it.
2.	javax.swing.* :-  Provides a set of "lightweight" (all-Java language) components that, to the maximum degree possible, work the same on all platforms. For extension of Jpanel I are going to use this class.
3.	java.awt.* :- Contains all of the classes for creating user interfaces and for painting graphics and images. A user interface object such as a button or a scrollbar is called, in AWT terminology, a component. The Component class is the root of all AWT components
4.	javax.swing.Timer :-  Fires one or more ActionEvents at specified intervals. For working with timer I are going to use this class .


2)	Creating the gameplay class  :- In this class I have implemented actionListener and keyListener for detecting the action of ball and keys
 I have defined  some private int variable like score , totalBricks , player position ball position etc. and a Boolean variable ‘play’ which will be  used in some condition latter.


3)Gameplay constructor :- I have defined a gameplay construcutor here 
To work with keyListener first I nedd to add the keyListner in the construcutor 
Next I have speicifed  delay of timer and then created a object for timer in our construcutor . 
Then I have initiated the timer.

4)Paint function :- This function ressemble our graphcs part of the program .it contain all the dimension and attributes of the borders , backgroung, map, padlle , score,ball . 
This function has two condition of winnig and losing the game.
Winning :- The player will win when the total number of bricks become zero . so at this moment it will show a message to user “You won, press enter to restart”.
Losing :- The player will losse when the ball will not bounce on slider , i.e it will exceeds its Y axis  position to 570+ . That time it will show a message “Game Over ” with score  and “press enter to restart”.

5)keyPressed Function :- As the name suggest , this function detects the key which user has press  right or left and according to that the slider moves . This function has 3 condition for 3 input.
Right key :- If user press right key , the slider will move towards right but only till X axis positon of slider is 600 pixels latter on it will not move.
Left Key:-  If user press Left key , the slider will move towards Left but only till the  X axis positon of  is 10 pixels latter on it will not move.
Enter Key:-  When the user will win or loose the game , then the user will press enter key , then the game will start from start with zero score.

6)keyReleased and KeyTyped unction :- this two function does not contribute in our  program but still I have to keep them as they are the part of keylistener, otherwise the program will throw error.

7)MoveLeft & MoveRight Method :- Here I have created this two method for movement of the slider. whenever the user press left or right arrow key the  will shift by 20 pixels accordingly.

8)ActionPerformed Function :-  This function is responsible for the movement of ball I have use some condition to increment or decrement the the postion of the ball hence giving it motion. 
 Then I have use 3 condition to keep the ball inside the frame. It will keep the ball in frame by reversing its direction. 

CONCLUSION:
1)	Brick breaker is simple and interactive game that helps us to get significant knowledge about 2D game development.
2)	From this assignment I got to know enough about java.awt library which Contains all of the classes for creating user interfaces and for painting graphics and images. 
3)	Brick Breaker was a successful educational experience that solidified our understanding of java.
