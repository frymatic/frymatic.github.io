# Internet of Things
[Back](https://www.woodyhooten.com)

![hackathon](https://i.imgur.com/Y0uiyLv.png)

Unit 2 is done! Kinda wish this unit was a little longer since it seems like a field that's going to be very important in the future. The microbit ASICs we worked with were pretty neat though. Here's the portfolio of Unit 2:
[github](https://github.com/frymatic/Internet-of-Things)

Like last time, for those curious about the full body of work, they can find it all in the dropbox for this course's classwork here:
[dropbox](https://www.dropbox.com/sh/20oetseuokictz7/AACu33oQrltq51L7O8bk2PKEa?dl=0)

Some questions from the professor:

## How have you organized your portfolio and why is it in this order?
For such a short unit, I just put everything that I worked on in there. After that, it's pretty much alphabetical, which is sorta nonsense if order was supposed to convey some theme. 

## Why have you chosen these particular pieces to demonstrate your learning? 
Most of these are components of the final IoT project where I was trying out various bits of functionality.

## What piece would you like to remove from this collection? Why?

Some of the practice problems probably don't deserve to see the light of day because they only received minor modification beyond their status off the shelf. 
![randomness](https://i.imgur.com/yfEIlGy.png)

## Which piece in your portfolio are you most proud of?

The one titled "hooten_stepwork.py", the IoT project we did. Pretty neat exercise to work with tight constraints (around 200 lines of python max per microbit program).

## What makes this your best piece?

I thought demonstrated the concept of a thing talking to another thing, as should be expected from an IoT solution.

```python
# core loop
while True:
    # win condition check
    if level > len(levels) - 1:
        endGame()

    # show player level/image
    display.show(levels[level])
   
    # button controls
    if button_a.is_pressed():
        if score < 10:
            display.show(str(score))
            sleep(200)
        else:
            display.scroll(str(score))
            sleep(200)
    elif button_b.is_pressed():
        # radio output
        radio.send('levelUp')
        # receiving player level += 1 
        sleep(100)
    
    # 1 step = 1 point
    if accelerometer.was_gesture("shake"):
        score += (1 * level)

    # listen for radio input
    incoming = radio.receive()
    if incoming == 'levelUp':
        level += 1  # basically, only others can cause you to win
```

## How did you go about creating it?

I built it starting from example applications for the microbit. Once I found a sufficient set of functions properly demonstrated, I blended them together into my own little IoT game. It's gonna be the next Pokémon GO, just you wait.

## What problems did you encounter? How did you solve them? 

With the microbit I ran into some issue with properly calling libraries, though I think this mostly stemmed from the fact that examples came from disparate locations, all observing separate conventions for how to use a given library.

## Of all the items included, which one was the hardest for you?   

The aforementioned StepWork game was probably the hardest. Honestly, the greatest difficulty came from navigating the various hardware issues that came with such a cheap piece of electronics. Some of it (ex: gesture detection was spotty) simply didn't work as advertised/expected. 

## What makes your strongest piece different from your weakest piece?

The overall design. Of the weaker pieces, most were targeted at testing a single feature. The best project had a rudimentary game designed for it, requiring the use of multiple features in concert. The was an actual user experience in mind, not simply testing whether the micro:bit works.

## What goals did you set for yourself? How well did you accomplish them?

Do something actually in the realm of what IoT is about: things, networked. Most of the projects around me were simply things, and a few were only internet. 

## What is the one thing you would like someone to notice about your portfolio? Why?

For Unit 2, I think I did a good header describing what I was building. I think that's pretty important.

## Do you feel that this collection of work really reflects your abilities and what you have achieved so far this year? Why or why not?

StepWork was an ok demonstration of my ability to design and code within tight constraints. However, I feel I could better demonstrate my ability in developing IoT if I had more devices available to test with. The Internet of Things is most interesting when lots of things are talking to one another.

[Home](https://www.woodyhooten.com)