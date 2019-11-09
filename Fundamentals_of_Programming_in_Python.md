# Fundamentals of Programming in Python
[Back](index.md)

![python](https://i.imgur.com/PbehiH2.png)

Unit 1 is done! I feel like I can say I have the Fundamentals of Python mastered, thanks to a pretty excellent class at Sierra College. Here's the portfolio of work so far:
[github](https://github.com/frymatic/Fundamentals-of-Python)

If you wanna see everything we've done though, this is probably a better starting point:
[dropbox](https://www.dropbox.com/sh/20oetseuokictz7/AACu33oQrltq51L7O8bk2PKEa?dl=0)

Some questions from the professor:

## How have you organized your portfolio and why is it in this order?
I started from the beginning, a very good place to start. Hello, world! I left a few things out that I found somewhat uninspiring for this showcase.

## Why have you chosen these particular pieces to demonstrate your learning? 
They're all that I've got!

## What piece would you like to remove from this collection? Why?

Perhaps some of the practice problems? They get a little tedious to navigate if you're just working on something at the very end.
![randomness](https://i.imgur.com/yfEIlGy.png)

## Which piece in your portfolio are you most proud of?

My Rock Paper Scissors game. 

## What makes this your best piece?

I thought it was a pretty good use of Dictionaries with nested lists to streamline the logic of determining wins.
```python
results = {
'rock':['paper','scissors'],
'paper':['scissors','rock'],
'scissors':['rock','paper']
}

# determine result of the round. rock beats scissors, paper beats rock, scissors beat paper
def compare(player, computer):

	if player == computer: # from first version, equivalent inputs always resolved as ties, still useful in more streamline version
		print("It's a tie! Play again.")
	elif results[player][1] == computer: # check win condition at index 1 against computer's choice relative to the player's input
		print("Player wins! Play again.") # proclaim the player as the winner
	else:
		print("Computer wins! Play again.") # proclaim the computer as the winner
```

## How did you go about creating it?

It first started as a partner project. In our initial pass, we had numerous If Elif trees to achieve the appropriate result. Then we streamlined individually. 

## What problems did you encounter? How did you solve them? 

We had some trouble with inputs. Try blocks did the trick.

## Of all the items included, which one was the hardest for you?   

The Password Locker. Flow Control got a little messy at times. I think it could probably be tightened up quite a bit given some time.

## What makes your strongest piece different from your weakest piece?

The percentage of the code written by me. With the practice problems it was fill in the blanks. The ones starting from scratch felt better in terms of learning due to having to own each part of the overall structure.

## What goals did you set for yourself? How well did you accomplish them?

Learn beyond the class wherever possible. I feel like I incorporate at least one thing outside the curriculum in each project reasonably well. 

## What is the one thing you would like someone to notice about your portfolio? Why?

My commenting. I believe I write comments that are not only descriptive, but also somewhat entertaining, which I think is likely to be a welcome change of pace in the working world. It's one thing to be good, it's another thing to be a good team mate.

## Do you feel that this collection of work really reflects your abilities and what you have achieved so far this year? Why or why not?

Maybe. Generally speaking, nothing stumped me to the point where I had to struggle. Those are the moments where I find I learn the most. I think the real challenges are ahead, and I'm kinda excited for them.

[Home](index.md)
