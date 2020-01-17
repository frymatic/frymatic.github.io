# Mobile Development
[Back](index.md)

The world is mobile first. The true power of computers and the internet may be in the hands of personal computers, but the broadest market for publishing is in the mobile experience. 

![InternetTrends]()


# Platform of Choice

Corona SDK, written in Lua.

Lua is very similar to Python in the way it is written. Not strongly typed, syntax is concise. Everything is a table, which is kinda cool (and not similar to Python).

You can make simple games like this pretty easily:
![Shooter Game](https://i.imgur.com/WMhpdYn.png)


Here's a code snippet (sorry for the screenshot, Markdown doesn't handle formatting Lua as well as Python) that I think demonstrated a tricky bit of trigonometry and ultimately memory management when drawing the bullets fired by tapping on the screen.
![Code Snippet](https://i.imgur.com/zABJnkI.png)

What's interesting about this code is how the animation is defined using the [transition.to() function of the Corona SDK](https://docs.coronalabs.com/api/library/transition/to.html). A transition moves an object from a starting point to an end point over a set period of time. Where the object should be placed on screen is calculated by the function, saving the developer the effort of manually drawing each frame of an object's movement. If you want all bullets that miss targets to fly off screen before disappearing, but you are determing where to aim the gun based on a tap that can only generated within the bounds of the screen (otherwise the player wouldn't be touching the screen).
![GIF](https://i.imgur.com/4GbMLd0.gif)

- [Fundamentals of Programming in Python](Fundamentals_of_Programming_in_Python.md)
- [Internet of Things (IoT)](iot.md)
- [Python Hackathon](Python_Hackathon.md)
