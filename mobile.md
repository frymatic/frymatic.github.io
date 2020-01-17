# Mobile Development
[Back](index.md)

The world is mobile first. The true power of computers and the internet may be in the hands of personal computers, but the broadest market for publishing has recently become the mobile experience. 

![InternetTrends](https://i.imgur.com/DHQCEKH.png)
From Mary Meeker's Annual [Internet Trends Report](https://www.bondcap.com/report/itr19/). For the first time with Bond Capital in 2019.

# Platform of Choice

Corona SDK (https://coronalabs.com/), written in Lua (https://www.lua.org/).
![Corona](https://i.imgur.com/VxHXdLK.png)


Lua is very similar to Python in the way it is written. Not strongly typed, syntax is concise. Everything is a table, which is kinda cool (and not similar to Python).

You can make simple games like this pretty easily:

![GIF](https://i.imgur.com/4GbMLd0.gif)

Here's a code snippet (sorry for the screenshot, Markdown doesn't handle formatting Lua as well as Python) that I think demonstrated a tricky bit of trigonometry and ultimately memory management when drawing the bullets fired by tapping on the screen.
![Code Snippet](https://i.imgur.com/zABJnkI.png)

What's interesting about this code is how the animation is defined using the [transition.to() function of the Corona SDK](https://docs.coronalabs.com/api/library/transition/to.html). A transition moves an object from a starting point to an end point over a set period of time. Where the object should be placed on screen is calculated by the function, saving the developer the effort of manually drawing each frame of an object's movement. If you want all bullets that miss targets to fly off screen before disappearing, but you are determing where to aim the gun based on a tap that can only generated within the bounds of the screen (otherwise the player wouldn't be touching the screen), then you are forced to calculate an end point for the transition that is off the map along the same trajectory. Similarly, you must also determine how long it should take the bullet to travel to that end point, which should be longer than the time it would take for the bullet to fly to the point where the screen was tapped to fire the bullet.

# Projects
- Target Shooter (discussed above)
- Fly Game (Flappy Bird clone)
Used [Sprite Objects in the Corona SDK](https://docs.coronalabs.com/api/type/SpriteObject/index.html) to animate my flying guy to flap every time the screen was tapped. He also animates while idling at the beginning of the game.

![Fly GIF](https://i.imgur.com/MaNiQIc.gif)
- Cow Pile
Utilized the [Box2D](https://box2d.org/) physics engine to make a game akin to [Cow Clicker](http://www.cowclicker.com/) as a final project for a mobile development class at Sierra College.

![Cow Pile](https://i.imgur.com/8J4GcL5.png)


