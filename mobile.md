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

What's interesting about this code is how the animation is defined using the [transition.to() function of the Corona SDK](https://docs.coronalabs.com/api/library/transition/to.html). A transition moves an object from a starting point to an end point over a set period of time. Where the object should be placed on screen is calculated by the function, saving the developer the effort of manually drawing each frame of an object's movement. If you want all bullets that miss targets to fly off screen before disappearing, but you are determing where to aim the gun based on a tap that can only generated within the bounds of the screen (otherwise the player wouldn't be touching the screen).


- [Fundamentals of Programming in Python](Fundamentals_of_Programming_in_Python.md)
- [Internet of Things (IoT)](iot.md)
- [Python Hackathon](Python_Hackathon.md)
